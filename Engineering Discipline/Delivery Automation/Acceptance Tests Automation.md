#
# Automate the Acceptance Tests

Acceptance test results are automatically generated.

## Implementation - 01

### Scope
Following implementation is applicable for any project who needs to generate and run Accpetance tests automatically. [Optional] If you are using AWS CodePipeline, accpetance tests can be run upon every successful release pipeline.

### Tools
- [Ghost Inspector](https://ghostinspector.com/)
- [Ghost Inspector Chrome Plugin](https://chrome.google.com/webstore/detail/ghost-inspector-automated/aicdiabnghjnejfempeinmnphllefehc)
- [AWS Code Pipeline](https://aws.amazon.com/codepipeline/)

### How?
- Create an account in Ghost Inspector website
- Add Ghost Inspector Chrome Plugin in to chrome browser
- Start separate feature flows using chrome plugin
- Do assertions while recording each flow
- Create a new stage in your AWS CodePipeine for Ghost Inspector 
- Integrate the Ghost Inspector with CodePipeline
- Link each acceptance test suite as separate stages

### Tips
- You can either create single test suite with all the feature test suite or create individual ones
- If you decide to use single test suite, you would not want to modify the codepipeline. You just have to use the chrome plugin to add more tests to existing test suite
- Downside for single test suite is that it is hard to distinguish between each feature test suit successes or failures
- AWS codepipeline has direct integration with Ghost Inspector

### Challenges
- Ghost Inspector free tier allows only 100 monthly test runs for and the result retention period is 3 months.