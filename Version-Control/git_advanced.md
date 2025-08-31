# Advanced Git Topics

---

## Git Rebase

Rebase is used to reapply commits on top of another base tip. It rewrites the commit history.

### Rebase Current Branch Onto Another Branch

```bash
git checkout <feature-branch>  
git rebase <base-branch>  
```

### Rebase with Conflict Resolution

```bash
# During rebase, conflicts may arise. Resolve conflicts and then run:  
git rebase --continue  

# To skip a conflicting commit:  
git rebase --skip  

# To abort the rebase process:  
git rebase --abort  
```

### Interactive Rebase

Interactive rebase is used to modify commit history.

```bash
git rebase -i <commit-hash-or-branch-name>  
```

* Options in Interactive Rebase:
  * `pick`: Use the commit as is.
  * `reword`: Edit the commit message.
  * `edit`: Modify the commit itself.
  * `squash`: Combine this commit with the previous one.
  * `drop`: Remove the commit.

---

## Git Reset

Undo changes in your working directory or staging area.

### Reset File from Staging Area

```bash
git reset <filename>  
```

### Reset to a Specific Commit (Keep Changes)

```bash
git reset --soft <commit-hash>  
```

### Reset to a Specific Commit (Discard Staged Changes)

```bash
git reset --mixed <commit-hash>  
```

### Reset to a Specific Commit (Discard All Changes)

```bash
git reset --hard <commit-hash>  
```

---

## Git Revert

Revert a commit by creating a new commit that undoes changes.

### Revert a Commit

```bash
git revert <commit-hash>  
```

### Revert Multiple Commits

```bash
git revert <commit-hash1> <commit-hash2>  
```

---

## Git Bisect

Find the commit that introduced a bug using binary search.

### Start Bisecting

```bash
git bisect start  
```

### Mark a Commit as Bad (Buggy)

```bash
git bisect bad  
```

### Mark a Commit as Good (Working)

```bash
git bisect good  
```

### Reset Bisect

```bash
git bisect reset  
```

---

## Git Tagging

Tags are used to mark specific points in commit history.

### Create a Lightweight Tag

```bash
git tag <tag-name>  
```

### Create an Annotated Tag

```bash
git tag -a <tag-name> -m "<tag message>"  
```

### List Tags

```bash
git tag  
```

### Push Tags to Remote

```bash
git push origin <tag-name>  
# Push all tags:  
git push --tags  
```

### Delete a Tag Locally

```bash
git tag -d <tag-name>  
```

### Delete a Tag Remotely

```bash
git push origin --delete <tag-name>  
```

---

Happy Learning😊!
