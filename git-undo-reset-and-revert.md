# Git Undo, Reset, and Revert Commands

Use the command that matches where the change is. `restore` changes files or the
index, `reset` moves the current branch pointer, and `revert` creates a new
commit that undoes an earlier commit.

## Discard changes in the working tree

```bash
# Discard unstaged edits to one tracked file; this cannot be undone easily.
git restore <file_name>

# Discard unstaged edits to every tracked file in the current directory.
git restore .
```

## Unstage changes and keep the edits

```bash
# Remove a file from the staging area without changing its contents.
git restore --staged <file_name>

# Unstage all staged changes while keeping the edits in the working tree.
git restore --staged .
```

## Undo a local commit

```bash
# Move HEAD back one commit; keep the changes, unstaged (the default --mixed mode).
git reset HEAD~1

# Move HEAD back one commit but keep the changes staged.
git reset --soft HEAD~1

# Move HEAD back one commit and discard its changes from the index and working tree.
# Destructive: use only when you are certain those changes are no longer needed.
git reset --hard HEAD~1
```

## Match a local branch to its remote

```bash
# Replace the current branch and working tree with origin/dev.
# Destructive: this discards local commits and uncommitted changes.
git fetch origin
git reset --hard origin/dev
```

Replace `dev` with the remote branch you intend to match. Check `git status`
and `git branch --show-current` before running this command.

## Undo a commit without rewriting history

```bash
# Create a new commit that reverses the changes introduced by the given commit.
git revert <commit-id>
```

Prefer `git revert` for commits that have already been shared with others. It
preserves the existing history and records the undo as a new commit.
