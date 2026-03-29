name: git
description: Perform common Git operations including cloning a repository, creating a branch, committing changes, and pushing to a remote repository.

## When to Use
Use this skill when the user asks to:
- clone a repository
- create or switch branches
- commit code changes
- push commits to a remote repository

Examples:
- "Clone this repo and create a branch"
- "Commit and push these changes"
- "Create a new feature branch"

## Workflow

### 1. Clone Repository
If the repository does not exist locally:

git clone <repository_url>
cd <repository_name>

### 2. Create or Switch Branch

Check branches:
git branch

Create new branch:
git checkout -b <branch_name>

Switch branch:
git checkout <branch_name>

### 3. Stage Changes

Stage everything:
git add .

Or specific file:
git add <file>

### 4. Commit Changes

git commit -m "commit message"

Commit message guidelines:
- short summary
- present tense
- describe what changed

Example:
git commit -m "Add authentication middleware"

### 5. Push Branch

First push:
git push -u origin <branch_name>

Later pushes:
git push

## Validation

Before pushing run:

git status
git log --oneline -5

Ensure:
- correct branch
- intended files staged
- meaningful commit message

## Common Errors

Push rejected:
git pull origin <branch_name> --rebase

Wrong branch:
git checkout <branch_name>

## Safety Rules

- Do not force push unless explicitly requested.
- Confirm repository URL before cloning.
- Verify branch name before pushing.