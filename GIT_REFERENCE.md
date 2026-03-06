# Git Quick Reference

## Setup
| Command | What it does |
|---------|-------------|
| `git init` | Turn a folder into a git repository |
| `git config --global user.name "Name"` | Set your name for commits |
| `git config --global user.email "email"` | Set your email for commits |

## The Core Workflow
| Command | What it does |
|---------|-------------|
| `git status` | Show what's staged, modified, and untracked |
| `git add <file>` | Stage a file (snapshot it for the next commit) |
| `git add file1 file2` | Stage multiple specific files |
| `git commit -m "message"` | Commit staged files with an inline message |
| `git commit` | Commit staged files (opens editor for message) |

## Inspecting History
| Command | What it does |
|---------|-------------|
| `git log` | Show full commit history |
| `git log --oneline` | Show commit history, one line per commit |
| `git log --stat` | Show commits with file names and line counts |
| `git log -p` | Show commits with full diffs |
| `git show <commit-id>` | Show details and diff for one specific commit |
| `git diff` | Show unstaged changes (working dir vs staging) |
| `git diff --staged` | Show staged changes (staging vs last commit) |
| `git diff <id1> <id2>` | Compare two commits |

## Undoing Things
| Command | What it does |
|---------|-------------|
| `git restore --staged <file>` | Unstage a file (keep the changes on disk) |
| `git checkout -- <file>` | Discard unstaged changes (revert file to staged/last commit) |

## Key Concepts
- **Working directory** — your actual files on disk
- **Staging area (index)** — snapshot of what will go into the next commit
- **Repository (.git/)** — permanent history of all commits
- **Commit ID (SHA)** — unique hash identifying each commit (e.g., `e914c8c`)
- **Conventional commits** — message prefixes: `feat:`, `fix:`, `docs:`, `chore:`
