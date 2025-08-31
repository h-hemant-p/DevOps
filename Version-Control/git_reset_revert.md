## **Git Reset and Revert**

##### **Git Reset**

* `git reset` is used to undo changes in a Git repository.
* It can modify the  **HEAD** ,  **index (staging area)** , and  **working directory** .
* Three main modes:  **soft** ,  **mixed** , and  **hard** .

###### **Git Reset Modes**

| Command                                 | Effect on HEAD       | Effect on Staging (Index) | Effect on Working Directory       |
| --------------------------------------- | -------------------- | ------------------------- | --------------------------------- |
| `git reset --soft <commit>`           | Moves HEAD to commit | Keeps staged changes      | Keeps working directory unchanged |
| `git reset --mixed <commit>`(default) | Moves HEAD to commit | Unstages changes          | Keeps working directory unchanged |
| `git reset --hard <commit>`           | Moves HEAD to commit | Clears staging area       | Discards all changes              |

###### **Basic Reset Commands**

1. **Reset to a previous commit (keep changes staged)**

   ```sh
   git reset --soft <commit-hash>
   ```

   * Moves HEAD back but keeps files staged.
   * Useful if you want to change the last commit message.
2. **Reset to a previous commit (unstage changes but keep files)**

   ```sh
   git reset --mixed <commit-hash>
   ```

   * Moves HEAD back and unstages changes.
   * Default behavior of `git reset <commit-hash>`.
3. **Reset to a previous commit (discard all changes)**

   ```sh
   git reset --hard <commit-hash>
   ```

   * Moves HEAD back, unstages changes, and deletes all modifications.
   * **WARNING:** This is irreversible unless changes are backed up.
4. **Reset only specific files (unstage changes)**

   ```sh
   git reset <file>
   ```

   * Removes the file from the staging area but keeps changes in the working directory.

###### **Undoing Commits**

1. **Undo the last commit (keep changes staged)**

   ```sh
   git reset --soft HEAD~1
   ```

   * Rolls back one commit but keeps changes staged.
2. **Undo the last commit (keep changes but unstage them)**

   ```sh
   git reset HEAD~1
   ```

   * Unstages changes but keeps them in the working directory.
3. **Undo the last commit (discard changes completely)**

   ```sh
   git reset --hard HEAD~1
   ```

   * Deletes the last commit and all associated changes.

###### **Recovering After `git reset --hard`**

* If you accidentally run `git reset --hard`, you may be able to recover with:

  ```sh
  git reflog
  ```

  * Find the commit hash before the reset and restore it:
    ```sh
    git reset --hard <commit-hash>
    ```

---

##### **Git Revert**

* `git revert` creates a **new commit** that undoes the changes of a previous commit.
* Unlike `git reset`, it  **does not modify history** , making it safe for shared branches.

###### **Basic Git Revert Commands**

1. **Revert a single commit**

   ```sh
   git revert <commit-hash>
   ```

   * Creates a new commit that undoes the changes of the specified commit.
   * Example:
     ```sh
     git revert abc1234
     ```
2. **Revert multiple commits (one by one)**

   ```sh
   git revert <commit1> <commit2> <commit3>
   ```

   * Creates separate revert commits for each specified commit.
3. **Revert multiple commits (as a single commit)**

   ```sh
   git revert -n <commit1> <commit2>
   git commit -m "Reverted multiple commits"
   ```

   * `-n` (`--no-commit`) applies the changes without committing them.
   * You can review and modify changes before committing.
4. **Revert the last commit**

   ```sh
   git revert HEAD
   ```

   * Undoes the most recent commit.
5. **Revert a commit without opening an editor**

   ```sh
   git revert -m 1 <merge-commit-hash>
   ```

   * Used for **reverting a merge commit** (choose **parent commit** using `-m`).
   * `-m 1` usually selects the main branch as the parent.

###### **Handling Revert Conflicts**

1. If conflicts occur, Git will pause the revert.
2. Manually resolve conflicts in affected files.
3. Add the resolved files:
   ```sh
   git add <resolved-file>
   ```
4. Complete the revert:
   ```sh
   git revert --continue
   ```
5. If you want to cancel the revert:
   ```sh
   git revert --abort
   ```

---

##### **When to Use `git revert` vs. `git reset`?**

| Command        | Use Case                                                                         |
| -------------- | -------------------------------------------------------------------------------- |
| `git revert` | Undo changes**without modifying commit history**(safe for shared branches) |
| `git reset`  | Removes commits from history (not safe for shared branches)                      |
