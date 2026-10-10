# 2. Create a Branch
## Create a new branch
git branch feature/login

## Create a branch from a specific branch
git branch feature/payment main

## Create and switch to a new branch
git switch -c feature/login

## Create and switch to a branch from a specific starting branch
git switch -c feature/payment main

## Create a local branch that tracks an existing remote branch
git switch --track origin/feature/payment