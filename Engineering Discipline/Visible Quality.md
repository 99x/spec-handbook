# New Features are Automated as a Regression Test Suite

Acceptance tests for new features are automated and maintained as a regression test suite. Coverage levels are incrementing over time.

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


#
# Integrate a Central Code Quality Analysis Tool 

Central code quality analysis tool is integrated to monitor continuously. Overall quality indicators follow upward trend during current quarter.
