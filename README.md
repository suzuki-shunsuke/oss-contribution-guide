# oss-contribution-guide

Guide to create GitHub Issues and Pull Requests for OSS Contribution

- Read the project's contribution guide
- Show the thankfulness
- Use English
- Create an Issue before creating a Pull Request
- Describe the detail as much as possible. Don't neglect to explain
- Use GitHub Flavored Markdown properly. Especially, fenced code blocks should be used
- Use the project Issue Template. Don't ignore the issue template
- Describe **WHY** and **Background** in your Feature Request
- Write good `How to reproduce`

## Show the thankfulness

I'm not good at English and my vocabulary is poor, but there are several phrases to show your thankfulness.

- Thank you for your great project!
- Thank you for your review!
- Thank you for your quick reply!
- Thank you for your quick fix!
- Thank you for your explanation!
- Thank you!
- etc

## Use English

This depends on the project, but if English is used in the project you should use English.
For example, even if the project author is Japanese, you shouldn't use Japanese if English is used in the project.

If you aren't good at English, you can translate your comment into English with Machine Translator such as DeepL and write both in comment.

## Create an Issue before creating a Pull Request

You should create an Issue and describe your proposal or a bug and disucss how to implement or how to solve the problem before creating a Pull Request.
You can discuss the detail of the implementation in the Pull Request, but you should describe the background of the pull request in the Issue.

Of course, there are some exception such as fixing typo.

## Describe the detail as much as possible. Don't neglect to explain

The lack of the information would make the unneeded conversation and misunderstanding.
You should be careful maintainers can handle the issue comfortably.

## Use GitHub Flavored Markdown properly. Especially, fenced code blocks should be used

[Fenced code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks) make the comment easy to read.
The readability of code without fenced block is terrible.

## Use the project Issue Template. Don't ignore the issue template

Using the Issue Template, maintainers can get required information and communicate with you comfortably.
If the Issue Template is ignored, maintainers can't get required information and unneeded conversation and misunderstanding would be required.

## Describe **WHY** and **Background** in your Feature Request

You should describe not only what is needed but also why this is needed and the background you think the feature is needed.

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
Everyone should be able to execute and reproduce the problem according to `How to reproduce`.
Code shouldn't be partial, because partial code isn't be executable.

Private resources shouldn't be used in `Hot to reproduce` if it isn't needed.
For example, if you can reproduce the issue with public Docker images, private Docker images shouldn't be used.

`Expected Behavior` and `Actual Behavior` should be clear.
For example, the report such as `an error occurs` and `the tool doesn't work` is ambiguous.
If an error occurs, you should paste the command and standard (error) output.
The screenshot may also be helpful, but a text in the screenshot can't be copied so you should paste the output as text too.

## Reference

- https://opensource.guide/how-to-contribute/#how-to-submit-a-contribution

## LICENSE

[MIT](LICENSE)
