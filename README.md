# Axia GitOps Capstone Project - CI Pipeline

## Project Overview
A lightweight internal service with a fully automated
GitOps workflow using Trello, GitHub, and GitHub Actions.

## Architecture
- Task Tracking: Trello
- Source Control: GitHub
- Automation: GitHub Actions (Lint + Test)

## Workflow
1. Pick task from Trello Backlog
2. Create feature branch
3. Write code and commit with Trello ID
4. Open Pull Request
5. CI pipeline runs automatically
6. Merge only when all checks pass

## Commit Convention
[TRELLO-###] Short description

## Setup Instructions
1. Clone the repo
2. Run: pip install -r requirements.txt
3. Run tests: pytest test_app.py -v

## Reflection

### 1. What is GitOps and why does it matter?
GitOps is a way of managing software where Git is the
single source of truth for everything in your project.
Instead of manually deploying code or making changes
directly on servers, every change goes through Git first.
This means every update is tracked, reviewed and
reversible. It matters because it brings order and
visibility to software delivery. Teams can see exactly
what changed, who changed it and when. For a small
engineering team struggling with inconsistent practices,
GitOps creates a clear process everyone follows. It
reduces human error, speeds up delivery and makes
onboarding new developers much easier because
everything is documented in the repository itself.

### 2. How does CI/CD improve code quality?
CI/CD stands for Continuous Integration and Continuous
Delivery. CI automatically runs tests and checks every
time a developer pushes code. This means broken code
gets caught immediately before it reaches the main
codebase. In this project GitHub Actions runs flake8
for linting and pytest for testing on every pull request.
If either check fails the merge is blocked automatically.
This removes the human error of forgetting to run tests
locally. CD extends this by automating deployment after
tests pass. Together CI/CD creates a safety net that
enforces quality consistently across the entire team
without relying on manual discipline alone.

### 3. What is linting and why is it important?
Linting is the process of automatically checking your
code for style errors, formatting issues and potential
bugs before it runs. In this project we use flake8 which
checks Python code against the PEP 8 style guide. Linting
is important because it enforces consistency across a
team. When every developer follows the same style rules
the codebase becomes easier to read and maintain.
It also catches simple mistakes early like unused
variables or missing spaces that could cause confusion
later. Without linting different developers write in
different styles making the code harder to understand
and review over time.

### 4. How does branch strategy prevent broken code?
A branch strategy means developers never work directly
on the main branch. Instead every new feature or fix
gets its own separate branch. In this project we use
the convention feature/TRELLO-###-description so every
branch is linked to a specific task. This prevents broken
code from reaching main because changes only merge after
passing CI checks and being reviewed through a pull
request. If something breaks on a feature branch it stays
isolated there and does not affect the stable codebase.
This gives the team confidence that main always contains
working reliable code ready for deployment at any time.

### 5. What did you learn from this project?
This project taught me that professional software
delivery is about much more than writing code. I learned
how to design a complete GitOps workflow connecting task
management, source control and automation together. I
understood how GitHub Actions works as an automation
engine that enforces quality on every single commit.
I learned the importance of documentation for onboarding
and team consistency. Most importantly I shifted my
thinking from just making code work locally to making
systems that work reliably for an entire team. This
project gave me practical experience with the tools and
practices that real engineering teams use every day.
