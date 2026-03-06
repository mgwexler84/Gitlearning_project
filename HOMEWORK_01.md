# Homework 01: Solo Git Workflow Practice

## The Assignment
Build a new project from scratch — completely separate from this one — to prove you can do the full local-to-GitHub workflow on your own.

## Steps

1. Create a new folder somewhere on your machine (e.g., `~/CodingStuff/python-practice`)
2. Initialize it as a git repo
3. Create a `.gitignore` that excludes:
   - `.DS_Store`
   - `__pycache__/` (Python's compiled file cache)
   - `.env`
4. Create a file called `hello.py` with a simple Python hello world program
5. Stage and commit both files with a meaningful commit message (use conventional commits format)
6. Create a GitHub repo called `python-practice` and link it to your local folder
7. Push your commit to GitHub

## How I'll Check Your Work
When you're done, tell me and I'll run these commands to verify:

- `gh repo view mgwexler84/python-practice` — confirms the repo exists
- I'll look at your commit history and messages
- I'll check that your `.gitignore` has the right entries
- I'll check that `hello.py` actually runs

## Bonus (optional)
- Make a second commit that changes `hello.py` to ask the user their name and greet them
- Push that too, so you have 2 commits in the remote history

## Hints
- Refer to GIT_REFERENCE.md if you get stuck
- `git status` is your best friend — run it between every step
- Python hello world is just: `print("Hello, World!")`
