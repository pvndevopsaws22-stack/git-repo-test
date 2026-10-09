1. List Branches
List local branches
Displays all local branches in the current repository.

git branch
List all local and remote branches
Displays local branches and remote-tracking branches.

git branch -a
List remote branches
Displays remote-tracking branches.

git branch -r
Show the current branch
Displays the name of the currently checked-out branch.

git branch --show-current
2. Create a Branch
Create a new branch
Creates a branch named feature/login from the current commit without switching to it.

git branch feature/login
Create a branch from a specific branch
Creates feature/payment starting from the current commit of main.

git branch feature/payment main
Note: Creating a branch does not automatically switch to it.

3. Switch Branches
Switch to an existing branch
Switches to the main branch.

git switch main
Create and switch to a new branch
Creates feature/login and switches to it immediately.

git switch -c feature/login
Older equivalent commands
The git checkout command can also be used to switch branches or create and switch to a branch.

Switch to an existing branch:

git checkout main
Create and switch to a new branch:

git checkout -b feature/login
Recommendation: Prefer git switch for switching branches and git restore for restoring files.

4. View Branch Details
Show branches and their latest commits
Displays each local branch with its latest commit information.

git branch -v
Show branches with tracking information
Displays local branches, their latest commits, and upstream tracking information when configured.

git branch -vv
Show merged branches
Lists branches whose commits have been merged into the current branch.

git branch --merged
Show branches not yet merged
Lists branches that have commits not merged into the current branch.

git branch --no-merged
