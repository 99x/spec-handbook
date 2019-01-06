#
# Automate Release Notes Generation

Release notes are automatically generated.

## Implementation - 01

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

