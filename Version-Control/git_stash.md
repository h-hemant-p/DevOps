## **Git Stash**

* `git stash` temporarily stores uncommitted changes without committing them.
* It allows switching branches or performing other Git operations without losing work.

##### **Git Stash Commands**

* **Save current changes**

  ```sh
  git stash
  ```

  * Stashes all tracked changes (modified and staged files).
  * Untracked files are not included by default.
* **List stashes**

  ```sh
  git stash list
  ```

  * Shows all saved stashes.
  * Example output:
    ```
    stash@{0}: WIP on main: abc1234 Commit message
    stash@{1}: WIP on feature-branch: def5678 Another commit
    ```
* **Apply stash (restore latest stash without removing it)**

  ```sh
  git stash apply
  ```
* **Apply a specific stash**

  ```sh
  git stash apply stash@{2}
  ```
* **Apply and remove latest stash**

  ```sh
  git stash pop
  ```

  * Applies the latest stash and removes it from the list.
* **Remove a specific stash**

  ```sh
  git stash drop stash@{1}
  ```
* **Clear all stashes**

  ```sh
  git stash clear
  ```
* **Stash untracked files too**

```sh
# Includes untracked files in the stash.
git stash -u
```

* **Stash with a message**

  ```sh
  git stash push -m "WIP: Fixing bug in feature-x"
  ```

  * Useful for identifying stashes later.
* **Create a stash and apply it to a different branch**

  ```sh
  git stash
  git checkout other-branch
  git stash pop
  ```
* **Show stash details**

  ```sh
  git stash show -p stash@{0}
  ```

  * Shows what changes were saved in a stash.
* **Create a stash for only specific files**

  ```sh
  git stash push -m "Partial stash" -- file1.txt file2.txt
  ```
