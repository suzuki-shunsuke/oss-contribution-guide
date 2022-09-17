# oss-contribution-guide

Guide to create GitHub Issues and Pull Requests for OSS Contribution

## Index

- [Read the project's contribution guide](#read-the-projects-contribution-guide)
- [Show the thankfulness](#show-the-thankfulness)
- [Use English](#use-english)
- [Create an Issue before creating a Pull Request](#create-an-issue-before-creating-a-pull-request)
- [Describe the detail as much as possible. Don't neglect to explain](#describe-the-detail-as-much-as-possible-dont-neglect-to-explain)
- [Use GitHub Flavored Markdown properly](#use-github-flavored-markdown-properly)
- [Use Issue Templates](#use-issue-templates)
- [Describe **WHY** and **Background** in your Feature Request](#describe-why-and-background-in-your-feature-request)
- [Write good `How to reproduce`](#write-good-how-to-reproduce)

## Read the project's contribution guide

First, you should check and follow the project's contribution guide such as `CONTRIBUTING.md`.

## Show the thankfulness

There are several phrases to show your thankfulness.

- Thank you for your great project!
- Thank you for your review!
- Thank you for your quick reply!
- Thank you for your quick fix!
- Thank you for your explanation!
- Thank you!
- etc

You should respect and appreciate all OSS maintainers.

## Use English

If English is used in the project you should use English.
For example, even if the project author is Japanese, you shouldn't use Japanese if English is used in the project.

Machine Translator such as [DeepL](https://www.deepl.com/translator) would help you.

## Create an Issue before creating a Pull Request

You should create an Issue and describe your proposal or a bug and disucss how to implement or how to solve the problem before creating a Pull Request.
You can discuss the detail of the implementation in the Pull Request, but you should describe the background of the pull request in the Issue.

Of course, there are some exceptions such as fixing typo.

## Describe the detail as much as possible. Don't neglect to explain

The lack of information would make unneeded conversation and misunderstanding.
It would help if you were careful maintainers can handle the Issue comfortably.

## Use GitHub Flavored Markdown properly

Especially, you should use [fenced code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).
Fenced code blocks make a comment easy to read.
The readability of code without fenced block is terrible.

## Use Issue Templates

Using Issue Templates, maintainers can get the required information and communicate with you comfortably.
If you ignore them, maintainers may misunderstand the issue or they would have to ask you some questions to get the required information.

If there is no issue template in the project, you should structure the description according to some common issue template.

## Describe **WHY** and **Background** in your Feature Request

It would help if you described not only what is needed but also why this is needed and the background you think the feature is necessary.

[Reference: XY problem](https://en.wikipedia.org/wiki/XY_problem)

If there is a workaround, you should describe it and why it isn't enough.

Sometimes your problem would be solved without new feature development.

## Write good `How to reproduce`

You should write the following information.

- Environment
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

## Related Articles

- https://opensource.guide/how-to-contribute/#how-to-submit-a-contribution

## LICENSE

[MIT](LICENSE)
