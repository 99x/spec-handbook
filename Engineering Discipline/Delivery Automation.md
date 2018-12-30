Delivery Automation
===================

# Guideline  [01]

Any code change may trigger a build, and any successful build can be deployed to staging automatically.

## Implementation Suggessions
- [Implementation 01](#g01-implementation---01)

## [G01] Implementation - 01

### Scope
Following implementation is applicable for the projects that uses AWS to manage their CI/CD pipeline.

### Tools
- [GitHub](https://github.com)
- [AWS Code Build](https://aws.amazon.com/codebuild/)
- [AWS Code Pipeline](https://aws.amazon.com/codepipeline/)

### How?
- Create Code Build projects for frontend and backend projects
- [Optional] If the backend consists of multiple microservices, create Code Build project for each
- Link Code Build project with GitHub via Webhook (Configure from Code Build console)
- Create Code Pipeline projects for Production/Staging/Dev environmets
- Link Code Build projects in each Code Pipeline as steps (Parallel/Serial)
- Link the GitHub branch (e.g. Production/Staging/Dev) that corresponding CodePipeline should be triggered

### Tips
- Configure CodeBuild status update to be published to GitHub
- Configure manual approvals if you think both frontend and backend deployments are unnecessary for each release
- Add manual approval steps in the Code Pipeline particularly for production release
- Send emails to interested parties when the CodePipeline is finished
- Canary deployment can be added by ticking off canary deployment check on the microservice (AWS API Gateway Level)

### Challenges
- Rollbacks are not yet directly supported as part of CodePipeline
- We need to use CodeDeploy project to configure rollbacks with the pipeline


# Guideline  [02]

Acceptance test results are automatically generated.

## Implementation Suggessions
- [Implementation 01](#g02-implementation---01)

## [G02] Implementation - 01

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

# Guideline  [03]

Release notes are automatically generated.

## Implementation Suggessions
- [Implementation 01](#g03-implementation---01)

## [G03] Implementation - 01

### Scope
Applicable to projects that uses GitHub as the source control system

### Tools
- [Gren Robot](https://www.npmjs.com/package/github-release-notes)
- [AWS Code Pipeline](https://aws.amazon.com/codepipeline/)

### How?
- Install github-release-notes npm globally
- You can arrange github issues in milestones (This is just one option)
- Close issues related to the milestone before the release
- Do a latest tag release 
- Attach gren tool to the CI/CD pipeline
- Once CI/CD is succesful perform gren release that will create a release notes in GitHub

### Tips
- Arranging tasks in milestones will give more clarity for release notes output
- Attach labels for each type of task E.g Feature, Bug Fix, Technical Task to obtain category wise separation in the release note

### Challenges
- No major challenges other than plug the release note generator to the build pipeline

