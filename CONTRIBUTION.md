# Contributing Guide

## Welcome to the Team!
This guide explains exactly how to contribute
to this project the right way.

## Branching Rules
- Never push directly to main
- Always create a feature branch first
- Branch format: feature/TRELLO-###-description

## Examples of correct branch names
feature/TRELLO-001-setup-repository
feature/TRELLO-002-create-ci-pipeline
feature/TRELLO-003-write-tests

## Commit Format
Every commit must reference a Trello ID like this:
[TRELLO-###] Short description of what you did

## Examples of correct commits
[TRELLO-001] Setup repository structure and starter files
[TRELLO-002] Add GitHub Actions CI pipeline
[TRELLO-003] Add 8 passing tests to test suite

## Pull Request Process
1. Create your feature branch
2. Make your changes
3. Commit with Trello ID in message
4. Push branch to GitHub
5. Open Pull Request with Trello ID in title
6. Wait for CI checks to pass
7. Request review
8. Merge only when approved and CI is green

## CI/CD Pipeline Explanation
Our pipeline runs automatically on every push and PR.
It does three things in this exact order:

1. Install Dependencies
   pip install -r requirements.txt

2. Lint Code
   flake8 app.py test_app.py
   This checks code style and formatting.
   Failed lint means red build and blocked merge.

3. Run Tests
   pytest test_app.py -v
   This runs all 8 tests automatically.
   Failed test means red build and blocked merge.

## Coding Standards
- Follow PEP 8 Python style guide
- Use clear and descriptive function names
- No unused imports allowed
- Maximum line length is 79 characters
- Always add a blank line between functions

## Failure Handling
If your CI build fails:
1. Click the failed check on GitHub
2. Read the error message carefully
3. Fix the issue on your local machine
4. Commit the fix with a clear message
5. Push again and CI will re-run automatically

## Code Review Rules
- Every PR must be reviewed before merging
- Leave helpful and constructive comments
- Approve only when CI is fully green
- Never merge your own PR without review
