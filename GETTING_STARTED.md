# Getting Started Guide

## Welcome!
This guide will get you up and running in under 1 hour.

## Step 1 — Install Python
Download Python 3.11 from https://python.org
Make sure to tick "Add Python to PATH" during installation.

## Step 2 — Install Git
Download Git from https://git-scm.com
This gives you Git Bash to run commands.

## Step 3 — Clone the Repository
Open Git Bash and type:

git clone https://github.com/danieldMimi-tech/axia-gitops-capstone
cd axia-gitops-capstone

## Step 4 — Install Dependencies
pip install -r requirements.txt

## Step 5 — Run Tests
pytest test_app.py -v

All 8 tests should pass like this:
test_health PASSED
test_sum PASSED
test_reverse PASSED
test_sum_with_negative PASSED
test_sum_with_zero PASSED
test_reverse_empty_string PASSED
test_reverse_single_char PASSED
test_health_returns_200 PASSED

## Step 6 — Create Your Branch
git checkout -b feature/TRELLO-00X-your-task-name

## Step 7 — Make Changes and Save
git add .
git commit -m "[TRELLO-00X] Your commit message"
git push origin feature/TRELLO-00X-your-task-name

## Step 8 — Create a Pull Request
1. Go to github.com and open the repository
2. Click "Compare and Pull Request"
3. Add a clear title with your Trello ID
4. Click "Create Pull Request"
5. Wait for CI checks to pass
6. Then merge

## Troubleshooting
Problem: Tests are failing
Solution: Run pip install -r requirements.txt again

Problem: Lint is failing
Solution: Check your code for extra spaces or long lines

Problem: CI not running
Solution: Make sure ci.yml is inside .github/workflows/ folder

Problem: Cannot push to main
Solution: You must create a feature branch first. Never push directly to main.
