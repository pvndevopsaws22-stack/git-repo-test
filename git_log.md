# Basic and Common Git Log Commands

## Show the commit history
```bash
git log
```

## Show commits in a compact, one-line format
```bash
git log --oneline
```

## Show the latest five commits
```bash
git log -5 --oneline
```

## Show history as a graph, including all branches
```bash
git log --oneline --graph --decorate --all
```

## Show files changed in each commit
```bash
git log --stat
```

## Show commits by a specific author
```bash
git log --author="Name"
```

## Show commits from a date range
```bash
git log --since="2 weeks ago"
git log --after="2026-01-01" --before="2026-02-01"
```

## Show history for a specific file
```bash
git log --oneline -- path/to/file
```

## Search commit messages for a word or phrase
```bash
git log --oneline --grep="bug fix"
```