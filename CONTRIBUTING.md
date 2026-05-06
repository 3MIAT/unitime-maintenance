\# Contributing Guidelines



\## Branching Strategy



\- `main` branch contains stable production-ready code.

\- `develop` branch is used for integration and testing.

\- `feature/\*` branches are used for implementing new features or bug fixes.



Example:

feature/instructor-conflict-report



\---



\## Development Workflow



1\. Pull the latest changes from `develop`

2\. Create a new feature branch

3\. Implement changes

4\. Commit changes with meaningful messages

5\. Push branch to GitHub

6\. Open a Pull Request to `develop`

7\. Wait for review and approval before merge



\---



\## Commit Message Convention



Use clear commit messages with prefixes:



\- `feat:` for new features

\- `fix:` for bug fixes

\- `docs:` for documentation

\- `refactor:` for code improvements

\- `test:` for testing



Examples:



feat: add instructor conflict detection service



docs: add contributing guidelines



fix: resolve null pointer in conflict report



\---



\## Pull Request Rules



\- Every change must be submitted through a Pull Request

\- At least one team member must review the PR

\- PR description must explain:

&#x20; - what was changed

&#x20; - why it was changed

&#x20; - affected modules/classes

\- All tests must pass before merge



\---



\## Code Review Guidelines



Reviewers should check:



\- Code readability

\- Naming conventions

\- Null safety

\- Edge cases

\- Test coverage

\- Integration risks



Reviews must contain meaningful comments and suggestions.



\---



\## Merge Policy



\- Direct pushes to `main` are not allowed

\- Only reviewed Pull Requests can be merged

\- All review comments must be resolved before merging



\---



\## Branch Protection



\- `main` and `develop` branches should be protected

\- Force push is not allowed

\- Pull request approval is required before merge

