Visible Quality
=============== 

## Guideline [01]

Critical areas of the system are covered with unit, integration and functional tests as applicable.


## Guideline [02]

Continuous Integration is in place and tests are automatically executed upon builds. Commits are stopped if a test/build is broken, until fixed.


## Guideline [03]

Central code quality analysis tool is integrated to monitor continuously. Overall quality indicators follow upward trend during current quarter.


## Guideline [04]

Team is aware and practices of TDD in developing new code modules. All new code written is testable with proper dependency handling techniques.


## Guideline [05]

Acceptance tests for new features are automated and maintained as a regression test suite. Coverage levels are incrementing over time.

## Implementation Suggessions
- [Implementation 01](#implementation---01)

## Implementation - 01

### Scope 
- Following implementation is applicable for the projects that uses AWS to manage their CI/CD pipeline.. 

### Tools
- [AWS Code Build](https://aws.amazon.com/codebuild/)
- [AWS Code Pipeline](https://www.hotjar.com)
- [Ghost Inspector](https://ghostinspector.com/)

### How?
- Go to ghost inspector home page and create an account
- Install chrome recorder plugin
- Create a new Test Suite
- Create a new Test Case
- Use the installed chrome recorder to record the acceptance test 
- Edit the test case where ever needed
- Go to the code pipeline project where you need to add run newly created acceptance tests.
- Add a new stage in the code pipeline project to run acceptance tests.
- Add a new action on the "Acceptance test" stage.
- Select the "Ghost Inspector UI Testing" as action provider
- Connect into the Ghost inspector account.
- select the test suite previously created and click on integrate.
- Now the Automated acceptance tests are fully integrated into the code pipeline itself so that the tests will be automatically triggered upon each release.

### Tips
- N/A

### Challenges
- Ghost Inspector free version has following limitations
    100 Test Runs Monthly
    1 Team Member
    3 month result retention
for more information : https://ghostinspector.com/pricing/
