## **Git Cherry-Picking**

* `git cherry-pick` allows you to apply specific commits from one branch to another.
* Useful for selecting bug fixes or features without merging an entire branch.

###### **Cherry-Picking Commands**

1. **Cherry-pick a single commit**

   ```sh
   git cherry-pick <commit-hash>
   ```

   * Applies the specified commit to the current branch.
   * Example:
     ```sh
     git cherry-pick abc1234
     ```
2. **Cherry-pick multiple commits**

   ```sh
   git cherry-pick <commit1> <commit2> <commit3>
   ```

   * Example:
     ```sh
     git cherry-pick a1b2c3 d4e5f6 g7h8i9
     ```
3. **Cherry-pick a range of commits**

   ```sh
   git cherry-pick <start-commit>^..<end-commit>
   ```

   * Picks all commits from `<start-commit>` **to** `<end-commit>`.
   * Example:
     ```sh
     git cherry-pick abc1234^..xyz7890
     ```
   * The `^` ensures that the start commit is included.

###### **Handling Cherry-Pick Conflicts**

1. **If conflicts occur:**
   * Git will pause the cherry-pick and show the conflict.
   * Resolve the conflicts in the affected files.
   * Use `git add <resolved-file>` to stage resolved changes.
   * Continue the cherry-pick:
     ```sh
     git cherry-pick --continue
     ```
   * If you want to abort:
     ```sh
     git cherry-pick --abort
     ```

###### **Cherry-Picking with Options**

1. **Cherry-pick without committing**

   ```sh
   git cherry-pick -n <commit-hash>
   ```

   * Applies changes but does **not** create a commit, allowing manual modifications.
2. **Cherry-pick with a custom commit message**

   ```sh
   git cherry-pick -e <commit-hash>
   ```

   * Opens an editor to modify the commit message.
3. **Skip a commit if it fails**

   ```sh
   git cherry-pick --skip
   ```

   * Useful when conflicts are too difficult to resolve.
4. **Cherry-pick while keeping original commit info**

   ```sh
   git cherry-pick -x <commit-hash>
   ```

   * Adds a reference to the original commit in the commit message.
