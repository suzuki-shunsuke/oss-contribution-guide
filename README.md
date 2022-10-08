# oss-contribution-guide

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
- [Avoid a force push after starting the review](#avoid-a-force-push-after-starting-the-review)
- [Separate commits that code was created or updated by command](#separate-commits-that-code-was-created-or-updated-by-command)
- [Related Articles](#related-articles)

## Read the project's contribution guide

First, you should check and follow the project's contribution guide such as `CONTRIBUTING.md`.

## Use English

If English is used in the project you should use English.
For example, even if the project author is Japanese, you shouldn't use Japanese if English is used in the project.

Machine Translator such as [DeepL](https://www.deepl.com/translator) would help you.

## Create an Issue before creating a Pull Request

You should create an Issue and describe your proposal or a bug and disucss how to implement or how to solve the problem before creating a Pull Request.
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
Code shouldn't be partial, because partial code isn't executable.

Private resources shouldn't be used in `How to reproduce` if it isn't needed.
For example, if you can reproduce the issue with public Docker images, you shouldn't use private Docker images.

`Expected Behavior` and `Actual Behavior` should be clear.
For example, a report such as `an error occurs` and `the tool doesn't work` is ambiguous.
If an error occurs, you should paste the command and standard (error) output.
A screenshot may also be helpful, but a text in the screenshot can't be copied so you should paste the output as text too.

## Avoid a force push after starting the review

After maintainers start reviewing or you ask maintainers for their review, you shouldn't do a force push,
because a force push makes it difficult for maintainers to review the diff.
Instead of a force push, you should push new commits, and then maintainers can review the diff.

## Separate commits that code was created or updated by command

If you generate some codes by command, you should separate commits for the change with other changes.
And you should show the command in the commit message.
This makes changes easy to understand and review.

## Related Articles

- https://opensource.guide/how-to-contribute/#how-to-submit-a-contribution

## LICENSE

[MIT](LICENSE)
