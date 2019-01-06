# Analyze Code Quality Automatically

Code quality is analyzed automatically at the development environment (IDE). A common ruleset used for analysis is shared across the team members.

#
# Implementation - 01

### Scope
Following implementation is applicable to the projects that use GIT as the version control system. 

### Tools
- [Codacy](https://www.codacy.com/)
- [JSLint](https://www.jslint.com/)
- [ESLint](https://eslint.org/)

### How?
- GitHub is linked with Codacy
- Codacy code quality analysis is run on every PR submission
- Codacy will comment refactoring suggessions below the PR automatically 
- IDE is configured with the same ruleset of JSLint/ESLint which is configured with Codacy

### Tips
- Disable PR merging unless automated code quality test is passed
- Disable PR merging unless manual review is approved
- Select a suitable set of rules in Codacy code quality settings

### Result
![codacity](https://user-images.githubusercontent.com/2338919/50731236-8dde7600-1185-11e9-9e90-f59e456835b1.png)

### Challenges
- Codacy allows only 4 team members in the free tier 