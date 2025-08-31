
## Git Merge, Pull, and Rebase

##### Git Merge

Merging is the process of integrating changes from one branch into another. It preserves the history of both branches and creates a merge commit if necessary.

###### **Basic Merge Commands**

* **Merge a branch into the current branch:**

```bash
git merge <branch_name>
```

* **Merge the branch into main:**

```bash
git checkout main
git merge <branch_name>
```

* **Fast-Forward Merge (If No Diverging Commits Exist):**

```bash
git checkout main
git merge --ff-only <branch_name>
```

* **Merge with No Fast-Forward (Always Creates a Merge Commit):**

```bash
git merge --no-ff <branch_name>
```

* **Abort a Merge in Case of Issues:**

```bash
git merge --abort
```

##### Git Pull

`git pull` is used to fetch and merge changes from a remote repository.

###### **Basic Pull Commands**

* **Fetch and merge changes from the remote tracking branch:**

```bash
git pull origin <branch_name>
```

* **Fetch changes without merging (useful for inspecting changes first):**

```bash
git fetch origin <branch_name>
```

* **Pull with Rebase Instead of Merge:**

```bash
git pull --rebase origin <branch_name>
```

* **Resolve Pull Conflicts:**
  * Edit conflicting files.
  * Add resolved files:
    ```bash
    git add <resolved-files>
    ```
  * Continue the rebase:
    ```bash
    git rebase --continue
    ```
  * If necessary, abort the rebase:
    ```bash
    git rebase --abort
    ```

##### Git Rebase

Rebasing is the process of moving or combining commits to maintain a clean, linear commit history.

###### **Basic Rebase Commands**

* **Rebase the current branch onto another branch:**

```bash
git checkout <branch_name>
git rebase main
```

* **Abort a rebase if something goes wrong:**

```bash
git rebase --abort
```

* **Skip a conflicting commit during rebase:**

```bash
git rebase --skip
```

* **Continue rebase after resolving conflicts:**

```bash
git add <resolved-files>
git rebase --continue
```

##### **Git Rebase vs Merge Conflicts**

During a rebase or merge, conflicts often arise.

###### **Rebase Conflict Resolution Steps**

1. **Start the Rebase:**
   ```bash
   git rebase <branch>  
   ```
2. **Resolve Conflicts:**
   Edit conflicting files.
3. **Mark Conflicts Resolved:**
   ```bash
   git add <resolved-files>  
   git rebase --continue  
   ```

###### **Merge Conflict Resolution Steps**

1. **Start the Merge:**
   ```bash
   git merge <branch>  
   ```
2. **Resolve Conflicts:**
   Edit conflicting files.
3. **Commit Changes:**
   ```bash
   git commit  
   ```

##### Git Merge vs Rebase

| **Feature** | **Merge**                 | **Rebase**                  |
| ----------------- | ------------------------------- | --------------------------------- |
| History           | Creates a merge commit.         | Rewrites commit history.          |
| Use Case          | Keep all commits from branches. | Maintain a linear commit history. |
| Conflicts         | Resolved during merge.          | Resolved during rebase process.   |

---

## Advanced Git Merge and Rebase Concepts

### **Interactive Rebase**

Allows you to modify commit history.

```bash
git rebase -i HEAD~<number_of_commits>
```

* **pick** – Keep the commit as is.
* **reword** – Change the commit message.
* **edit** – Modify the commit.
* **squash** – Merge this commit into the previous one.
* **fixup** – Like squash but discards commit message.

### **Merging a Specific Commit**

```bash
git cherry-pick <commit-hash>
```

### **Undo a Merge**

```bash
git reset --hard ORIG_HEAD
```

### **Git Rebasing Onto an Upstream Branch**

Rebase a branch to align with changes in an upstream branch.

#### **Steps:**

1. Fetch Changes from Upstream:
   ```bash
   git fetch upstream  
   ```
2. Rebase Current Branch:
   ```bash
   git rebase upstream/<branch-name>  
   ```

---
