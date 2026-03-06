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

## Remotes (GitHub)
| Command | What it does |
|---------|-------------|
| `git remote add origin <url>` | Link local repo to a remote (e.g., GitHub) |
| `git remote -v` | Show linked remotes (fetch and push URLs) |
| `git push -u origin main` | Push commits to remote (first time, sets default) |
| `git push` | Push commits to remote (after `-u` is set) |
| `gh repo create <name> --public --source=.` | Create GitHub repo and link to current folder |
| `gh repo create <name> --public --clone` | Create GitHub repo and clone it locally |
| `gh repo clone <user>/<repo>` | Clone an existing GitHub repo to your machine |
| `gh repo list` | List your GitHub repos |
| `gh repo view <user>/<repo>` | Show details about a GitHub repo |
| `gh repo delete <user>/<repo> --yes` | Delete a GitHub repo |
| `gh auth login` | Log into GitHub from the command line |
| `gh auth status` | Check your GitHub login status and permissions |

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
- **origin** — conventional name for your primary remote (just a name, not a keyword)
- **Remote** — a hosted copy of your repo (e.g., on GitHub). Your local repo knows about it, but it doesn't know about you until you push
- **-u (--set-upstream)** — saves the default remote+branch so future `git push` needs no arguments
- **`git push` sends ALL commits** on a branch that the remote doesn't have — you can't push individual commits

## Vi Survival Guide (for when git opens an editor)
| Key | What it does |
|-----|-------------|
| `i` | Enter insert mode (start typing) |
| `Esc` | Exit insert mode |
| `:wq` + Enter | Save and quit |
| `:q!` + Enter | Quit without saving |
