# Advanced Git Concepts

---

## Git Hooks

Git hooks are scripts that run automatically on certain Git events.

### Common Hooks

* **Pre-commit hook:** Runs before a commit is created.
* **Pre-push hook:** Runs before pushing changes to a remote repository.
* **Post-merge hook:** Runs after merging changes.

### Set Up a Hook

Hooks are stored in the `.git/hooks` directory.

```bash
cd .git/hooks  
# Example: Create a pre-commit hook  
echo "echo 'Running pre-commit hook'" > pre-commit  
chmod +x pre-commit  
```

---

## Git Submodules

Submodules allow you to include a Git repository inside another repository.

### Add a Submodule

```bash
git submodule add <repository-url> <path>  
```

### Initialize and Update Submodules

```bash
git submodule init  
git submodule update  
```

### Remove a Submodule

```bash
git submodule deinit <path-to-submodule>  
rm -rf <path-to-submodule> .git/modules/<path-to-submodule>  
git rm --cached <path-to-submodule>  
```

---

## Git Worktrees

Worktrees allow you to check out multiple branches in the same repository.

### Create a New Worktree

```bash
git worktree add <path> <branch-name>  
```

### Remove a Worktree

```bash
git worktree remove <path>  
```

---

## Git Squash Merging

Combine all commits from a branch into a single commit during merging.

### Perform a Squash Merge

```bash
git merge --squash <branch-name>  
git commit -m "Squash merge commit"  
```

---

## Git Blame

Git blame helps you track who made changes to specific lines in a file.

### Basic Blame Command

```bash
git blame <file>  
```

### Ignore Certain Revisions

```bash
git blame <file> --ignore-revs-file <file-with-revs-to-ignore>  
```

---

## Git Bundle

Git bundle is used to create a single file that contains the entire repository or specific commits.

### Create a Bundle

```bash
git bundle create <file.bundle> --all  
```

### Clone a Repository from a Bundle

```bash
git clone <file.bundle> <repository-path>  
```

---

## Git Clean

Clean untracked files and directories from your working directory.

### Remove Untracked Files

```bash
git clean -f  
```

### Remove Untracked Files and Directories

```bash
git clean -fd  
```

---

---

## Git Garbage Collection

Optimize your repository by cleaning up unnecessary files and optimizing the database.

### Run Garbage Collection

```bash
git gc  
```

### Aggressive Garbage Collection

```bash
git gc --aggressive  
```

---

## Git Advanced Diffing

Compare changes between different commits, branches, or files.

### Compare Two Branches

```bash
git diff <branch1> <branch2>  
```

### Show Changes Introduced by a Commit

```bash
git diff <commit-hash>  
```

### Word-Level Diff

```bash
git diff --word-diff  
```

---

## Git Patch

Git patches are used to share changes without pushing to a remote repository.

### Create a Patch

```bash
git diff > changes.patch  
```

### Apply a Patch

```bash
git apply changes.patch  
```

### Create a Commit Patch

```bash
git format-patch <base-branch>  
```

### Apply a Commit Patch

```bash
git am <patch-file>  
```

---

## Git Reflog

The `reflog` tracks every change in the HEAD, allowing you to recover lost commits.

### View Reflog History

```bash
git reflog  
```

### Restore a Lost Commit

```bash
git checkout <commit-hash-from-reflog>  
```

---

## Git Notes

Add additional information to commits without altering commit messages.

### Add a Note

```bash
git notes add -m "Additional information about this commit"  
```

### View Notes

```bash
git notes show <commit-hash>  
```

### Merge Notes

```bash
git notes merge <ref>  
```

---

## Git Bisect Automation

Automate the process of finding bugs using a script.

### Automate Bisecting

```bash
git bisect start  
git bisect bad  
git bisect good <commit-hash>  
git bisect run <script>  
```

---

## Git Hooks Advanced Use Cases

1. **Pre-push Hook:** Run tests before pushing.
   ```bash
   echo "npm test" > .git/hooks/pre-push  
   chmod +x .git/hooks/pre-push  
   ```
2. **Post-commit Hook:** Automatically sign-off commits.
   ```bash
   echo "git commit --amend --no-edit --signoff" > .git/hooks/post-commit  
   chmod +x .git/hooks/post-commit  
   ```

---

## Git Credential Management

Store credentials securely for authenticated operations.

### Cache Credentials Temporarily

```bash
git config --global credential.helper cache  
```

### Store Credentials Permanently

```bash
git config --global credential.helper store  
```

---

## Git Workflow Strategies

### Gitflow Workflow

* Separate branches for  **features** ,  **releases** , and  **hotfixes** .

```bash
git branch feature/<feature-name>  
```

### Forking Workflow

* Contributors fork the repository, make changes, and submit pull requests.

### Trunk-Based Development

* Developers commit directly to the main branch and use feature toggles.

---

1.

---

## Git Aliases

Create shortcuts for commonly used Git commands.

### Add an Alias

```bash
git config --global alias.<alias-name> "<command>"  
```

### Examples:

* Shorten `git status`:
  ```bash
  git config --global alias.st "status"  
  ```
* Shorten `git log` to display one-line commits:
  ```bash
  git config --global alias.lg "log --oneline --graph --all"  
  ```

---

Happy Learning😊!
