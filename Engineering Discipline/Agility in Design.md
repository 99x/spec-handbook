# Continuous Refactoring

Refactoring needs are identified through automation. A backlog for managing technical debt is maintained by the team.

## Implementation - 01

### Scope
Following implementation is applicable to the projects that use GIT as the version control system. 

### Tools
- [GitHub](https://github.com)
- [Codacy](https://www.codacy.com/)
- [Trello](https://trello.com/)

### How?
- GitHub is linked with Trello (via powerups) and Codacy
- Each Trello task has a corresponding GitHub issue linked via Issue Id
- Each PR is linked with GitHub Issue Id 
- Codacy code quality analysis is run on every PR submission
- Codacy will comment refactoring suggessions below the PR automatically 

### Tips
- Disable PR merging unless automated code quality test is passed
- Disable PR merging unless manual review is approved
- Select a suitable set of rules in Codacy code quality settings
- Track the Trello taks for refactoring with Labels e.g. Technical Task 

### Result
![codacity](https://user-images.githubusercontent.com/2338919/50731236-8dde7600-1185-11e9-9e90-f59e456835b1.png)

### Challenges
- Codacy allows only 4 team members in the free tier 
