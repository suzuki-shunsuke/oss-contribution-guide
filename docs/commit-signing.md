# Commit Signing

- [Signing commits - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)
- [Generating a new GPG key - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)
- [Adding a GPG key to your GitHub account - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account)
- [GitHub Branch protection rule - `Require signed commits`](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)

Some repositories enable the branch protection rule `Require signed commits`.
In that case, you have to sign all commits of your pull request.

## How to set up commit signing

If you haven't configured commit signing, please configure it according to the document.

- [Signing commits - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)
- [Generating a new GPG key - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)
- [Adding a GPG key to your GitHub account - GitHub](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account)

## How to fix your pull request with unsigned commits

If a repository enables `Require signed commits` but your pull request has unsigned commits, your pull request can't be merged as is.
To solve the issue, you have two options.

1. Rebase commits to sign them
1. Close the pull request and create a new one

The option 2 is simple but a little bothersome.
If your pull request includes merge commits and you're not familiar with Git, maybe the option 2 is better than the option 1.

In this document, we use Git CLI, but maybe there are more user friendly GUI tools or something.

### Option 1. Rebase commits to sign them

1. Please run the following command to rebase commits.

```sh
git rebase --exec 'git commit --amend -n --no-edit -S' -i HEAD~<The number of commits of the pull request>
```

e.g.

```sh
git rebase --exec 'git commit --amend -n --no-edit -S' -i HEAD~3
```

2. Then an editor is launched but you can close as is if the pull request doesn't include merge commits.

If the pull request includes merge commits, you should edit the interactive rebase to drop merge commits and remove exec commands for dropped commits.
Otherwise, merge commits are also rebased and they are included in your pull request's `Commits` and `Files changed`, which is hard to review the pull request.

![image](https://github.com/aquaproj/aqua-registry/assets/13323303/82d35ebd-edd4-4041-8c31-d9dbe83c7ea1)

e.g.

Before

```
pick dd4f4178f test
exec git commit --amend -n --no-edit -S
pick 0254f33ad chore: update dolthub/dolt v1.35.12 to v1.35.13 (#22505)
exec git commit --amend -n --no-edit -S
pick 45268c7a9 feat: add crates.io/cargo-expan (#22488)
exec git commit --amend -n --no-edit -S
pick cd71601cb feat: add nishanths/license (#22489)
exec git commit --amend -n --no-edit -S
pick d483dc33f feat: add crates.io/cargo-run-script (#22487)
exec git commit --amend -n --no-edit -S
pick beda86165 chore: update antham/gommit v2.9.0 to v2.10.0 (#22507)
exec git commit --amend -n --no-edit -S
pick d65a7ca4a fix(GoogleContainerTools/container-structure-test): follow up changes of container-structure-test v1.18.0 (#22508)
exec git commit --amend -n --no-edit -S
pick 447e69a9d test
exec git commit --amend -n --no-edit -S
```

After

```
pick dd4f4178f test
exec git commit --amend -n --no-edit -S
d 0254f33ad chore: update dolthub/dolt v1.35.12 to v1.35.13 (#22505)
d 45268c7a9 feat: add crates.io/cargo-expan (#22488)
d cd71601cb feat: add nishanths/license (#22489)
d d483dc33f feat: add crates.io/cargo-run-script (#22487)
d beda86165 chore: update antham/gommit v2.9.0 to v2.10.0 (#22507)
d d65a7ca4a fix(GoogleContainerTools/container-structure-test): follow up changes of container-structure-test v1.18.0 (#22508)
pick 447e69a9d test
exec git commit --amend -n --no-edit -S
```

If it fails to rebase by dropping merge commits and it's difficult to solve the issue, maybe you should create a new pull request.

3. Force push

```sh
git push origin <branch> --force
```

### Option 2. Close the pull request and create a new one

Checkout the latest base branch and create a new pull request.
You can create commits from scratch, but maybe [git cherry-pick](https://git-scm.com/docs/git-cherry-pick) command is useful.
You should exclude merge commits from the target of `git cherry-pick`.

e.g.

```sh
git checkout main
git pull upstream main
git switch -c <new branch>
git cherry-pick <commit hash> ... # Exclude merge commits
```
