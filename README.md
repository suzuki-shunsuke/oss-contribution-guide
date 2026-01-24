# oss-contribution-guide

[![Ask DeepWiki](https://img.shields.io/badge/Ask_DeepWiki-000000.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAyCAYAAAAnWDnqAAAAAXNSR0IArs4c6QAAA05JREFUaEPtmUtyEzEQhtWTQyQLHNak2AB7ZnyXZMEjXMGeK/AIi+QuHrMnbChYY7MIh8g01fJoopFb0uhhEqqcbWTp06/uv1saEDv4O3n3dV60RfP947Mm9/SQc0ICFQgzfc4CYZoTPAswgSJCCUJUnAAoRHOAUOcATwbmVLWdGoH//PB8mnKqScAhsD0kYP3j/Yt5LPQe2KvcXmGvRHcDnpxfL2zOYJ1mFwrryWTz0advv1Ut4CJgf5uhDuDj5eUcAUoahrdY/56ebRWeraTjMt/00Sh3UDtjgHtQNHwcRGOC98BJEAEymycmYcWwOprTgcB6VZ5JK5TAJ+fXGLBm3FDAmn6oPPjR4rKCAoJCal2eAiQp2x0vxTPB3ALO2CRkwmDy5WohzBDwSEFKRwPbknEggCPB/imwrycgxX2NzoMCHhPkDwqYMr9tRcP5qNrMZHkVnOjRMWwLCcr8ohBVb1OMjxLwGCvjTikrsBOiA6fNyCrm8V1rP93iVPpwaE+gO0SsWmPiXB+jikdf6SizrT5qKasx5j8ABbHpFTx+vFXp9EnYQmLx02h1QTTrl6eDqxLnGjporxl3NL3agEvXdT0WmEost648sQOYAeJS9Q7bfUVoMGnjo4AZdUMQku50McDcMWcBPvr0SzbTAFDfvJqwLzgxwATnCgnp4wDl6Aa+Ax283gghmj+vj7feE2KBBRMW3FzOpLOADl0Isb5587h/U4gGvkt5v60Z1VLG8BhYjbzRwyQZemwAd6cCR5/XFWLYZRIMpX39AR0tjaGGiGzLVyhse5C9RKC6ai42ppWPKiBagOvaYk8lO7DajerabOZP46Lby5wKjw1HCRx7p9sVMOWGzb/vA1hwiWc6jm3MvQDTogQkiqIhJV0nBQBTU+3okKCFDy9WwferkHjtxib7t3xIUQtHxnIwtx4mpg26/HfwVNVDb4oI9RHmx5WGelRVlrtiw43zboCLaxv46AZeB3IlTkwouebTr1y2NjSpHz68WNFjHvupy3q8TFn3Hos2IAk4Ju5dCo8B3wP7VPr/FGaKiG+T+v+TQqIrOqMTL1VdWV1DdmcbO8KXBz6esmYWYKPwDL5b5FA1a0hwapHiom0r/cKaoqr+27/XcrS5UwSMbQAAAABJRU5ErkJggg==)](https://deepwiki.com/suzuki-shunsuke/oss-contribution-guide)

Guide to creating GitHub Issues and Pull Requests for OSS Contribution

## Index

- [Read the project's contribution guide](#read-the-projects-contribution-guide)
- [Use English](#use-english)
- [Create an Issue before creating a Pull Request](#create-an-issue-before-creating-a-pull-request)
- [Use Issue Templates](#use-issue-templates)
- [Describe the detail as much as possible. Don't neglect to explain](#describe-the-detail-as-much-as-possible-dont-neglect-to-explain)
- [Use GitHub Flavored Markdown properly](#use-github-flavored-markdown-properly)
- [Describe **WHY** and **Background** in your Feature Request](#describe-why-and-background-in-your-feature-request)
- [Write good `How to reproduce`](#write-good-how-to-reproduce)
- [Don't do force pushes after opening pull requests](#dont-do-force-pushes-after-opening-pull-requests)
- [Separate commits that code was created or updated by command](#separate-commits-that-code-was-created-or-updated-by-command)
- [Sign commits](#sign-commits)
- [Add a newline at the end of file](#add-a-newline-at-the-end-of-file)
- [Allow changes to a pull request branch created from a fork](#allow-changes-to-a-pull-request-branch-created-from-a-fork)
- [Related Articles](#related-articles)

## Read the project's contribution guide

First, you should check and follow the project's contribution guide such as `CONTRIBUTING.md`.

## Use English

If English is used in the project you should use English.
For example, even if the project author is Japanese, you shouldn't use Japanese if English is used in the project.

Machine Translator such as [DeepL](https://www.deepl.com/translator) would help you.

## Create an Issue before creating a Pull Request

You should create an Issue and describe your proposal or a bug and discuss how to implement or how to solve the problem before creating a Pull Request.
You can discuss the detail of the implementation in the Pull Request, but you should describe the background of the pull request in the Issue.

Of course, there are some exceptions such as fixing typo.

## Use Issue Templates

Using Issue Templates, maintainers can get the required information and communicate with you comfortably.
If you ignore them, maintainers may misunderstand the issue or they would have to ask you some questions to get the required information.

If there is no issue template in the project, you should structure the description according to some common issue template.

## Describe the detail as much as possible. Don't neglect to explain

The lack of information would make unneeded conversation and misunderstanding.
It would help if you were careful maintainers can handle the Issue comfortably.

## Use GitHub Flavored Markdown properly

Especially, you should use [fenced code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).
Fenced code blocks make a comment easy to read.
The readability of code without fenced block is terrible.

## Describe **WHY** and **Background** in your Feature Request

It would help if you described not only what is needed but also why this is needed and the background you think the feature is necessary.

[Reference: XY problem](https://en.wikipedia.org/wiki/XY_problem)

If there is a workaround, you should describe it and why it isn't enough.

Sometimes your problem would be solved without new feature development.

## Write good `How to reproduce`

You should write the following information.

- Environment
  - OS (e.g. Windows, macOS, Ubuntu)
  - Arch (e.g. amd64, arm64)
  - tool versions: If multiple tools are used, you should write all tool versions
- Code
- command and result
- `Expected Behavior` and `Actual Behavior`
- Debug Log

If you try multiple versions, you should describe the result too.
`Code` and `command` should be minimum, reproducible, and executable.

Code unrelated to the issue should be removed.
Everyone should be able to execute the code and reproduce the problem according to `How to reproduce`.
Code shouldn't be partial because partial code isn't executable.

Private resources shouldn't be used in `How to reproduce` if it isn't needed.
For example, if you can reproduce the issue with public Docker images, you shouldn't use private Docker images.

`Expected Behavior` and `Actual Behavior` should be clear.
For example, a report such as `an error occurs` and `the tool doesn't work` is ambiguous.
If an error occurs, you should paste the command and standard (error) output.
A screenshot may also be helpful, but a text in the screenshot can't be copied so you should paste the output as text too.

## Don't do force pushes after opening pull requests

After opening pull requests, you shouldn't do force pushes
because force pushes make it difficult for maintainers to review the diff.
And if maintainers push commits to pull requests, your force push may eliminate maintainers' commits.
Instead of force pushes, you should push new commits, then maintainers can review the diff.

For example, when maintaiers request a change to you, if you push a new commit maintainers can review it easily, but if you do a force push, maintainers can't understand easily what is changed by force push so the review is difficult.

As an exception, if maintainers ask you to make commits history clean by rebasing, you should follow the request.

## Separate commits that code was created or updated by command

If you generate some codes by command, you should separate commits for the change with other changes.
And you should show the command in the commit message.
This makes changes easy to understand and review.

## Sign commits

[Please see `Commit Signing`](docs/commit-signing.md).

## Add a newline at the end of file

Please add a newline at the end of file.
Note that this doesn't mean add an empty line at the end of file.

<img width="230" alt="image" src="https://github.com/user-attachments/assets/ae45e4c6-fadf-481f-9ad4-927ed296343c">

The mark ⛔ means the file misses a newline at the end of file.

<img width="345" alt="image" src="https://github.com/user-attachments/assets/f569c07b-ef02-4009-8f94-c0ed44506e11">

> No newline at end of file

If you use VSCode, we recommend setting `"files.insertFinalNewline": true`.

https://stackoverflow.com/questions/44704968/visual-studio-code-insert-newline-at-the-end-of-files

Reference: [Why should text files end with a newline?](https://stackoverflow.com/a/729795/6364492)

## Allow changes to a pull request branch created from a fork

[Allowing changes to a pull request branch created from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork)

You should allow maintainers to push commits to your pull requests so that maintainers can collaborate with you well.

## Ask AI for Help

For simple questions or bugs, try asking AI tools such as DeepWiki or Claude Code. You may be able to resolve issues much faster without waiting for a maintainer’s response.

Sharing AI-generated investigation results or proposed fixes in an issue can also help maintainers. Rather than leaving everything to maintainers, actively using AI to investigate problems and showing a cooperative attitude can make it easier to receive support from them.

Whether AI tools are allowed naturally depends on each OSS project’s policy, but in OSS projects maintained by @suzuki-shunsuke, they are generally not restricted. Many of the projects maintained by @suzuki-shunsuke can be queried via DeepWiki:

- https://deepwiki.com/suzuki-shunsuke  
- https://deepwiki.com/aquaproj  
- https://deepwiki.com/csm-actions  
- https://deepwiki.com/lintnet  

## Have AI Review Issues and Pull Requests

Have AI review your issues and pull requests to check whether all necessary information is included and to improve their overall quality. The questions AI asks you to clarify are often the same things maintainers would want to confirm.

## Take Responsibility for AI-Generated Content

When using AI to create issues or pull requests, clearly disclose that AI was used. For example, you can add an AI agent as a co-author in commits or explicitly note when quoting AI-generated responses.

Before sharing AI-generated content, review it carefully and take responsibility for it. If maintainers ask questions about the content, responding with “I don’t know because it was generated by AI” is not acceptable.

## Related Articles

- https://opensource.guide/how-to-contribute/#how-to-submit-a-contribution

## LICENSE

[MIT](LICENSE)
