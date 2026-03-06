# Git Status and Git Diff — When and How to Use Them

## git status

**When to run it:** All the time. Before and after every git command. It's your dashboard.

**What it tells you:**
- Which branch you're on
- Files that are **staged** (ready to commit)
- Files that are **modified** but not staged
- Files that are **untracked** (new files git has never seen)

**Example output and what it means:**

```
On branch main
Changes to be committed:
    modified:   style.css          ← staged, will be included in next commit

Changes not staged for commit:
    modified:   index.html         ← changed on disk, but NOT staged yet

Untracked files:
    notes.txt                      ← brand new file, git doesn't know about it
```

**The clean state** — this is what you want to see after a successful commit:
```
On branch main
nothing to commit, working tree clean
```

## git diff

**There are three versions of this command, each comparing different layers:**

### 1. `git diff` (no flags)
- **Compares:** working directory vs staging area
- **Shows you:** changes you've made but haven't staged yet
- **When to use:** "What did I change since my last `git add`?"

### 2. `git diff --staged`
- **Compares:** staging area vs last commit
- **Shows you:** what will go into the next commit if you run `git commit` right now
- **When to use:** "What exactly am I about to commit?"

### 3. `git diff <commit1> <commit2>`
- **Compares:** any two commits
- **Shows you:** everything that changed between those two snapshots
- **When to use:** "What changed between these two points in history?"

## Reading diff output

```
diff --git a/index.html b/index.html    ← which file
--- a/index.html                        ← the "before" version
+++ b/index.html                        ← the "after" version
@@ -8,4 +8,5 @@                         ← line numbers (before and after)
 <body>
     <h1>Hello, World!</h1>
-    <p>Old text</p>                     ← line removed (minus sign)
+    <p>New text</p>                     ← line added (plus sign)
+    <p>Another new line</p>            ← line added
 </body>
```

- Lines starting with `-` were removed
- Lines starting with `+` were added
- Lines with no prefix are unchanged context (shown so you can see where changes are)

## The mental model

```
  Working Dir          Staging Area         Last Commit
  (your files)         (git add)            (git commit)
       |                    |                    |
       |--- git diff ------>|                    |
       |                    |--- git diff ------->|
       |                         --staged        |
```

Run `git status` to see WHAT changed. Run `git diff` to see HOW it changed.
