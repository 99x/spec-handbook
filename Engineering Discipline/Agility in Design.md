Agility in Design
=================

## Guideline [01]

Refactoring and standardization (generalization) needs are identified (preferably through automation). A backlog for managing technical debt is maintained by the team.

### Implementation Suggessions
- [Implementation 01](#implementation---01)

### Implementation - 01

#### Scope
Following implementation is applicable to the projects that use GIT as the version control system. 

#### Tools
- GitHub
- [Codacy](https://www.codacy.com/)
- [Trello](https://trello.com/)

#### How?
- GitHub is linked with Trello (via powerups) and Codacy
- Each Trello task has a corresponding GitHub issue linked via Issue Id
- Each PR is linked with GitHub Issue Id 
- Codacy code quality analysis is run on every PR submission
- Codacy will comment refactoring suggessions below the PR automatically 

#### Tips
- Disable PR merging unless automated code quality test is passed
- Disable PR merging unless manual review is approved
- Select a suitable set of rules in Codacy code quality settings
- Track the Trello taks for refactoring with Labels e.g. Technical Task 

#### Challenges
- Codacy allows only 4 team members in the free tier 
