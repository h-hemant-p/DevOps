# Git Interview Questions (200+ Questions with Answers)

This document contains **200+ Git interview questions** categorized into **Basic**, **Intermediate**, **Advanced**, and **Scenario-Based** sections, along with **answers** for each question.

---

## Basic Git Questions (1-50)

1. **What is Git?**

   - **Answer:** Git is a distributed version control system used to track changes in source code during software development.
2. **What is a repository in Git?**

   - **Answer:** A repository is a directory where Git tracks all the changes made to files in a project.
3. **What is the difference between Git and GitHub?**

   - **Answer:** Git is a version control system, while GitHub is a web-based platform that hosts Git repositories and provides additional collaboration features.
4. **How do you initialize a new Git repository?**

   - **Answer:** Use the command `git init`.
5. **What is a commit in Git?**

   - **Answer:** A commit is a snapshot of the changes made to the files in the repository at a particular point in time.
6. **How do you check the status of your working directory?**

   - **Answer:** Use the command `git status`.
7. **How do you add files to the staging area?**

   - **Answer:** Use the command `git add <file_name>` or `git add .` to add all changes.
8. **How do you commit changes?**

   - **Answer:** Use the command `git commit -m "Commit message"`.
9. **What is the difference between `git pull` and `git fetch`?**

   - **Answer:** `git fetch` downloads changes from the remote repository but does not merge them, while `git pull` downloads and merges the changes into the current branch.
10. **How do you push changes to a remote repository?**

    - **Answer:** Use the command `git push origin <branch_name>`.
11. **What is the `.gitignore` file, and how is it used?**

    - **Answer:** The `.gitignore` file specifies files and directories that Git should ignore. It is used to exclude files like logs, dependencies, and build artifacts from being tracked.
12. **How do you clone a repository?**

    - **Answer:** Use the command `git clone <repository_url>`.
13. **What is a branch in Git?**

    - **Answer:** A branch is a parallel version of the repository, allowing you to work on different features or fixes independently.
14. **How do you create a new branch?**

    - **Answer:** Use the command `git branch <branch_name>`.
15. **How do you switch to a different branch?**

    - **Answer:** Use the command `git checkout <branch_name>`.
16. **What is a merge in Git?**

    - **Answer:** Merging combines the changes from one branch into another.
17. **How do you merge a branch into the current branch?**

    - **Answer:** Use the command `git merge <branch_name>`.
18. **What is a conflict in Git, and how do you resolve it?**

    - **Answer:** A conflict occurs when Git cannot automatically merge changes. You need to manually edit the conflicting files, mark them as resolved with `git add`, and then commit the changes.
19. **What is a rebase in Git?**

    - **Answer:** Rebasing is the process of moving or combining a sequence of commits to a new base commit.
20. **How do you rebase a branch?**

    - **Answer:** Use the command `git rebase <base_branch>`.
21. **What is the difference between `git merge` and `git rebase`?**

    - **Answer:** `git merge` creates a new merge commit, while `git rebase` rewrites the commit history by applying commits on top of the base branch.
22. **How do you view the commit history?**

    - **Answer:** Use the command `git log`.
23. **What is a tag in Git?**

    - **Answer:** A tag is a reference to a specific point in the Git history, often used to mark release points.
24. **How do you create a tag?**

    - **Answer:** Use the command `git tag <tag_name>`.
25. **How do you push tags to a remote repository?**

    - **Answer:** Use the command `git push origin <tag_name>` or `git push origin --tags` to push all tags.
26. **What is the purpose of `git config`?**

    - **Answer:** `git config` is used to configure Git settings, such as user name, email, and default editor.
27. **How do you set your username and email in Git?**

    - **Answer:** Use the commands:
      ```bash
      git config --global user.name "Your Name"
      git config --global user.email "your.email@example.com"
      ```
28. **What is the difference between `git clone` and `git fork`?**

    - **Answer:** `git clone` creates a local copy of a repository, while `git fork` creates a copy of a repository on a remote platform like GitHub.
29. **How do you check the remote URL of a repository?**

    - **Answer:** Use the command `git remote -v`.
30. **What is the purpose of `git remote`?**

    - **Answer:** `git remote` is used to manage remote repositories (e.g., adding, renaming, or removing remotes).
31. **How do you add a remote repository?**

    - **Answer:** Use the command `git remote add <name> <url>`.
32. **What is the purpose of `git fetch`?**

    - **Answer:** `git fetch` downloads changes from a remote repository but does not merge them into the local branch.
33. **How do you delete a branch locally?**

    - **Answer:** Use the command `git branch -d <branch_name>`.
34. **How do you force delete a branch locally?**

    - **Answer:** Use the command `git branch -D <branch_name>`.
35. **What is the purpose of `git log --oneline`?**

    - **Answer:** It displays the commit history in a concise, one-line format.
36. **How do you view the changes made in the last commit?**

    - **Answer:** Use the command `git show`.
37. **What is the purpose of `git diff`?**

    - **Answer:** `git diff` shows the differences between files, commits, or branches.
38. **How do you compare the working directory with the staging area?**

    - **Answer:** Use the command `git diff`.
39. **How do you compare the staging area with the last commit?**

    - **Answer:** Use the command `git diff --cached`.
40. **What is the purpose of `git reset`?**

    - **Answer:** `git reset` is used to undo changes by moving the branch pointer to a specific commit.
41. **What is the difference between `git reset --soft`, `git reset --mixed`, and `git reset --hard`?**

    - **Answer:**
      - `git reset --soft`: Moves the branch pointer but keeps changes staged.
      - `git reset --mixed` (default): Moves the branch pointer and unstages changes.
      - `git reset --hard`: Moves the branch pointer and discards all changes.
42. **How do you undo the last commit but keep the changes in the working directory?**

    - **Answer:** Use the command `git reset --soft HEAD~1`.
43. **How do you undo the last commit and discard all changes?**

    - **Answer:** Use the command `git reset --hard HEAD~1`.
44. **What is the purpose of `git revert`?**

    - **Answer:** `git revert` creates a new commit that undoes the changes of a previous commit.
45. **How do you revert a specific commit?**

    - **Answer:** Use the command `git revert <commit_hash>`.
46. **What is the purpose of `git stash`?**

    - **Answer:** `git stash` temporarily saves changes that are not ready to be committed.
47. **How do you apply the most recent stash?**

    - **Answer:** Use the command `git stash apply`.
48. **How do you delete a stash?**

    - **Answer:** Use the command `git stash drop`.
49. **What is the purpose of `git cherry-pick`?**

    - **Answer:** `git cherry-pick` applies a specific commit from one branch to another.
50. **How do you cherry-pick a commit?**

    - **Answer:** Use the command `git cherry-pick <commit_hash>`.

---

## Intermediate Git Questions (51-100)

51. **What is a detached HEAD in Git?**

    - **Answer:** A detached HEAD occurs when you check out a specific commit rather than a branch. You are not on any branch, and new commits will not be associated with any branch.
52. **How do you recover from a detached HEAD state?**

    - **Answer:** Create a new branch using `git branch <branch_name>` or switch to an existing branch using `git checkout <branch_name>`.
53. **What is the purpose of `git reflog`?**

    - **Answer:** `git reflog` shows a log of all reference updates (e.g., branch checkouts, commits, resets) and helps recover lost commits or branches.
54. **How do you find a specific commit by message?**

    - **Answer:** Use the command `git log --grep="commit message"`.
55. **How do you find all commits by a specific author?**

    - **Answer:** Use the command `git log --author="Author Name"`.
56. **How do you find the commit where a specific string was added or removed?**

    - **Answer:** Use the command `git log -S "string"`.
57. **What is the purpose of `git bisect`?**

    - **Answer:** `git bisect` helps you find the commit that introduced a bug by performing a binary search through the commit history.
58. **How do you use `git bisect` to find a bug?**

    - **Answer:** Use the commands `git bisect start`, `git bisect bad`, and `git bisect good` to mark the bad and good commits, then follow the prompts to identify the faulty commit.
59. **What is the purpose of `git submodule`?**

    - **Answer:** `git submodule` allows you to include and manage external repositories within your main repository.
60. **How do you add a submodule to a repository?**

    - **Answer:** Use the command `git submodule add <repository_url>`.
61. **How do you update submodules in a repository?**

    - **Answer:** Use the command `git submodule update --init --recursive`.
62. **What is the purpose of `git worktree`?**

    - **Answer:** `git worktree` allows you to work on multiple branches simultaneously by creating separate working directories.
63. **How do you create a new worktree?**

    - **Answer:** Use the command `git worktree add <path> <branch_name>`.
64. **What is the purpose of `git blame`?**

    - **Answer:** `git blame` shows who last modified each line of a file and when.
65. **How do you use `git blame` to track changes in a file?**

    - **Answer:** Use the command `git blame <file_name>`.
66. **What is the purpose of `git clean`?**

    - **Answer:** `git clean` removes untracked files from the working directory.
67. **How do you remove untracked files?**

    - **Answer:** Use the command `git clean -f`.
68. **What is the purpose of `git archive`?**

    - **Answer:** `git archive` creates a compressed archive of a specific commit or branch.
69. **How do you create a zip archive of a branch?**

    - **Answer:** Use the command `git archive --format=zip --output=<file_name>.zip <branch_name>`.
70. **What is the purpose of `git grep`?**

    - **Answer:** `git grep` searches for a string in the working directory or repository history.
71. **How do you search for a string in the entire repository?**

    - **Answer:** Use the command `git grep "string"`.
72. **What is the purpose of `git patch`?**

    - **Answer:** A patch is a file that contains changes between commits or branches, which can be applied to another repository.
73. **How do you create a patch file?**

    - **Answer:** Use the command `git format-patch <commit_range>`.
74. **How do you apply a patch file?**

    - **Answer:** Use the command `git am <patch_file>`.
75. **What is the purpose of `git hooks`?**

    - **Answer:** Git hooks are scripts that run automatically before or after specific Git events (e.g., pre-commit, post-commit).
76. **How do you create a custom Git hook?**

    - **Answer:** Add a script to the `.git/hooks` directory with the appropriate hook name (e.g., `pre-commit`, `post-commit`).
77. **What is the purpose of `git filter-branch`?**

    - **Answer:** `git filter-branch` is used to rewrite Git history (e.g., removing sensitive data or splitting a repository).
78. **How do you remove a file from Git history using `git filter-branch`?**

    - **Answer:** Use the command:
      ```bash
      git filter-branch --force --index-filter \
      'git rm --cached --ignore-unmatch <file_name>' \
      --prune-empty --tag-name-filter cat -- --all
      ```
79. **What is the purpose of `git bundle`?**

    - **Answer:** `git bundle` creates a single file that contains a Git repository's data, which can be used for offline sharing.
80. **How do you create a Git bundle?**

    - **Answer:** Use the command `git bundle create <file_name>.bundle <branch_name>`.
81. **What is the purpose of `git fsck`?**

    - **Answer:** `git fsck` checks the integrity of the Git repository by verifying objects and connectivity.
82. **How do you check the integrity of a Git repository?**

    - **Answer:** Use the command `git fsck`.
83. **What is the purpose of `git gc`?**

    - **Answer:** `git gc` (garbage collection) optimizes the repository by cleaning up unnecessary files and compressing data.
84. **How do you run garbage collection in Git?**

    - **Answer:** Use the command `git gc`.
85. **What is the purpose of `git notes`?**

    - **Answer:** `git notes` allows you to add additional information (notes) to commits without modifying the commit history.
86. **How do you add a note to a commit?**

    - **Answer:** Use the command `git notes add -m "Note message" <commit_hash>`.
87. **What is the purpose of `git replace`?**

    - **Answer:** `git replace` allows you to replace one commit with another without modifying the commit history.
88. **How do you replace a commit using `git replace`?**

    - **Answer:** Use the command `git replace <old_commit> <new_commit>`.
89. **What is the purpose of `git sparse-checkout`?**

    - **Answer:** `git sparse-checkout` allows you to check out only specific files or directories from a repository.
90. **How do you enable sparse checkout in Git?**

    - **Answer:** Use the commands:
      ```bash
      git sparse-checkout init --cone
      git sparse-checkout set <directory>
      ```
91. **What is the purpose of `git switch`?**

    - **Answer:** `git switch` is used to switch between branches in Git (introduced in Git 2.23 as a more intuitive alternative to `git checkout`).
92. **How do you switch to a branch using `git switch`?**

    - **Answer:** Use the command `git switch <branch_name>`.
93. **What is the purpose of `git restore`?**

    - **Answer:** `git restore` is used to restore files in the working directory or staging area (introduced in Git 2.23 as a more intuitive alternative to `git checkout` and `git reset`).
94. **How do you restore a file in the working directory?**

    - **Answer:** Use the command `git restore <file_name>`.
95. **What is the purpose of `git range-diff`?**

    - **Answer:** `git range-diff` compares two commit ranges (e.g., before and after a rebase).
96. **How do you compare two commit ranges?**

    - **Answer:** Use the command `git range-diff <commit_range1> <commit_range2>`.
97. **What is the purpose of `git maintenance`?**

    - **Answer:** `git maintenance` is used to optimize and maintain a Git repository (introduced in Git 2.29).
98. **How do you run maintenance tasks in Git?**

    - **Answer:** Use the command `git maintenance run`.
99. **What is the purpose of `git switch --orphan`?**

    - **Answer:** `git switch --orphan` creates a new branch with no commit history.
100. **How do you create an orphan branch?**

     - **Answer:** Use the command `git switch --orphan <branch_name>`.

---

## Advanced Git Questions (101-150)

101. **What is the Git object model?**

     - **Answer:** Git's object model consists of four types of objects: blobs (file content), trees (directory structure), commits (snapshots), and tags (references to specific commits).
102. **What are the four types of Git objects?**

     - **Answer:** Blobs, trees, commits, and tags.
103. **How does Git store data internally?**

     - **Answer:** Git stores data as a series of snapshots in a content-addressable file system, where each object is identified by a SHA-1 hash.
104. **What is the purpose of `git cat-file`?**

     - **Answer:** `git cat-file` is used to inspect Git objects (e.g., blobs, trees, commits).
105. **How do you view the contents of a Git object?**

     - **Answer:** Use the command `git cat-file -p <object_hash>`.
106. **What is the purpose of `git hash-object`?**

     - **Answer:** `git hash-object` computes the SHA-1 hash of a file or content.
107. **How do you compute the hash of a file?**

     - **Answer:** Use the command `git hash-object <file_name>`.
108. **What is the purpose of `git update-index`?**

     - **Answer:** `git update-index` is used to modify the index (staging area) directly.
109. **How do you mark a file as unchanged in the index?**

     - **Answer:** Use the command `git update-index --assume-unchanged <file_name>`.
110. **What is the purpose of `git write-tree`?**

     - **Answer:** `git write-tree` writes the current index (staging area) to a tree object.
111. **How do you create a tree object from the index?**

     - **Answer:** Use the command `git write-tree`.
112. **What is the purpose of `git commit-tree`?**

     - **Answer:** `git commit-tree` creates a commit object from a tree object.
113. **How do you create a commit from a tree object?**

     - **Answer:** Use the command `git commit-tree <tree_hash> -m "Commit message"`.
114. **What is the purpose of `git symbolic-ref`?**

     - **Answer:** `git symbolic-ref` is used to read or modify symbolic references (e.g., HEAD).
115. **How do you view the current branch using `git symbolic-ref`?**

     - **Answer:** Use the command `git symbolic-ref HEAD`.
116. **What is the purpose of `git pack-objects`?**

     - **Answer:** `git pack-objects` is used to create packed archives of Git objects.
117. **How do you create a packed archive of objects?**

     - **Answer:** Use the command `git pack-objects <file_name>`.
118. **What is the purpose of `git unpack-objects`?**

     - **Answer:** `git unpack-objects` is used to unpack packed archives of Git objects.
119. **How do you unpack a packed archive?**

     - **Answer:** Use the command `git unpack-objects < <file_name>.pack`.
120. **What is the purpose of `git rev-parse`?**

     - **Answer:** `git rev-parse` is used to parse and manipulate Git references and object hashes.
121. **How do you resolve a branch name to a commit hash?**

     - **Answer:** Use the command `git rev-parse <branch_name>`.
122. **What is the purpose of `git show-ref`?**

     - **Answer:** `git show-ref` lists references (e.g., branches, tags) in the repository.
123. **How do you list all branches in the repository?**

     - **Answer:** Use the command `git show-ref --heads`.
124. **What is the purpose of `git for-each-ref`?**

     - **Answer:** `git for-each-ref` is used to iterate over references and perform actions.
125. **How do you list all tags in the repository?**

     - **Answer:** Use the command `git for-each-ref --format='%(refname)' refs/tags`.
126. **What is the purpose of `git describe`?**

     - **Answer:** `git describe` generates a human-readable name for a commit based on the nearest tag.
127. **How do you describe the current commit?**

     - **Answer:** Use the command `git describe`.
128. **What is the purpose of `git name-rev`?**

     - **Answer:** `git name-rev` converts a commit hash to a human-readable name.
129. **How do you convert a commit hash to a branch name?**

     - **Answer:** Use the command `git name-rev <commit_hash>`.
130. **What is the purpose of `git rerere`?**

     - **Answer:** `git rerere` (reuse recorded resolution) automates the resolution of merge conflicts.
131. **How do you enable `git rerere`?**

     - **Answer:** Use the command `git config --global rerere.enabled true`.
132. **What is the purpose of `git replace`?**

     - **Answer:** `git replace` allows you to replace one commit with another without modifying the commit history.
133. **How do you replace a commit using `git replace`?**

     - **Answer:** Use the command `git replace <old_commit> <new_commit>`.
134. **What is the purpose of `git notes`?**

     - **Answer:** `git notes` allows you to add additional information (notes) to commits without modifying the commit history.
135. **How do you add a note to a commit?**

     - **Answer:** Use the command `git notes add -m "Note message" <commit_hash>`.
136. **What is the purpose of `git sparse-checkout`?**

     - **Answer:** `git sparse-checkout` allows you to check out only specific files or directories from a repository.
137. **How do you enable sparse checkout in Git?**

     - **Answer:** Use the commands:

     ```bash
     git sparse-checkout init --cone
     git sparse-checkout set <directory>
     ```
138. **What is the purpose of `git switch`?**

     - **Answer:** `git switch` is used to switch between branches in Git (introduced in Git 2.23 as a more intuitive alternative to `git checkout`).
139. **How do you switch to a branch using `git switch`?**

     - **Answer:** Use the command `git switch <branch_name>`.
140. **What is the purpose of `git restore`?**

     - **Answer:** `git restore` is used to restore files in the working directory or staging area (introduced in Git 2.23 as a more intuitive alternative to `git checkout` and `git reset`).
141. **How do you restore a file in the working directory?**

     - **Answer:** Use the command `git restore <file_name>`.
142. **What is the purpose of `git range-diff`?**

     - **Answer:** `git range-diff` compares two commit ranges (e.g., before and after a rebase).
143. **How do you compare two commit ranges?**

     - **Answer:** Use the command `git range-diff <commit_range1> <commit_range2>`.
144. **What is the purpose of `git maintenance`?**

     - **Answer:** `git maintenance` is used to optimize and maintain a Git repository (introduced in Git 2.29).
145. **How do you run maintenance tasks in Git?**

     - **Answer:** Use the command `git maintenance run`.
146. **What is the purpose of `git switch --orphan`?**

     - **Answer:** `git switch --orphan` creates a new branch with no commit history.
147. **How do you create an orphan branch?**

     - **Answer:** Use the command `git switch --orphan <branch_name>`.
148. **What is the purpose of `git worktree`?**

     - **Answer:** `git worktree` allows you to work on multiple branches simultaneously by creating separate working directories.
149. **How do you create a new worktree?**

     - **Answer:** Use the command `git worktree add <path> <branch_name>`.
150. **What is the purpose of `git blame`?**

     - **Answer:** `git blame` shows who last modified each line of a file and when.

---

## Scenario-Based Git Questions (151-200)

151. **You accidentally committed sensitive data (e.g., passwords) to a repository. How would you remove it from the commit history?**
     - **Answer:** Use `git filter-branch` or `BFG Repo-Cleaner` to rewrite the commit history and remove the sensitive data.
152. **You want to undo the last commit but keep the changes in your working directory. How would you do it?**
     - **Answer:** Use `git reset --soft HEAD~1`.
153. **You want to undo the last commit and discard all changes. How would you do it?**
     - **Answer:** Use `git reset --hard HEAD~1`.
154. **You want to merge a branch but avoid a fast-forward merge. How would you do it?**
     - **Answer:** Use `git merge --no-ff <branch_name>`.
155. **You want to rebase a branch but stop at each commit to resolve conflicts. How would you do it?**
     - **Answer:** Use `git rebase -i` and mark commits with `edit`.
156. **You want to find out who introduced a specific line of code in a file. How would you do it?**
     - **Answer:** Use `git blame <file_name>`.
157. **You want to find all commits that contain a specific keyword in the commit message. How would you do it?**
     - **Answer:** Use `git log --grep="keyword"`.
158. **You want to find all commits that modified a specific file. How would you do it?**
     - **Answer:** Use `git log -- <file_name>`.
159. **You want to find the difference between two branches. How would you do it?**
     - **Answer:** Use `git diff <branch1>..<branch2>`.
160. **You want to find the difference between two specific commits. How would you do it?**
     - **Answer:** Use `git diff <commit1> <commit2>`.
161. **You want to find the commit that introduced a bug. How would you do it?**
     - **Answer:** Use `git bisect`.
162. **You want to find the most recent commit in a branch. How would you do it?**
     - **Answer:** Use `git log -1`.
163. **You want to find the commit where a specific file was deleted. How would you do it?**
     - **Answer:** Use `git log --diff-filter=D -- <file_name>`.
164. **You want to find the commit where a specific file was renamed. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
165. **You want to find the commit where a specific file was moved. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
166. **You want to find the commit where a specific file was added. How would you do it?**
     - **Answer:** Use `git log --diff-filter=A -- <file_name>`.
167. **You want to find the commit where a specific file was modified. How would you do it?**
     - **Answer:** Use `git log -- <file_name>`.
168. **You want to find the commit where a specific file was copied. How would you do it?**
     - **Answer:** Use `git log --diff-filter=C -- <file_name>`.
169. **You want to find the commit where a specific file was merged. How would you do it?**
     - **Answer:** Use `git log --merges -- <file_name>`.
170. **You want to find the commit where a specific file was rebased. How would you do it?**
     - **Answer:** Use `git reflog` to track rebase operations.
171. **You want to find the commit where a specific file was cherry-picked. How would you do it?**
     - **Answer:** Use `git log --grep="cherry-pick" -- <file_name>`.
172. **You want to find the commit where a specific file was reverted. How would you do it?**
     - **Answer:** Use `git log --grep="revert" -- <file_name>`.
173. **You want to find the commit where a specific file was amended. How would you do it?**
     - **Answer:** Use `git reflog` to track amended commits.
174. **You want to find the commit where a specific file was squashed. How would you do it?**
     - **Answer:** Use `git reflog` to track squash operations.
175. **You want to find the commit where a specific file was split. How would you do it?**
     - **Answer:** Use `git reflog` to track split operations.
176. **You want to find the commit where a specific file was filtered. How would you do it?**
     - **Answer:** Use `git reflog` to track filter operations.
177. **You want to find the commit where a specific file was rewritten. How would you do it?**
     - **Answer:** Use `git reflog` to track rewrite operations.
178. **You want to find the commit where a specific file was moved and renamed. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
179. **You want to find the commit where a specific file was moved and modified. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
180. **You want to find the commit where a specific file was moved and deleted. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
181. **You want to find the commit where a specific file was moved and copied. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
182. **You want to find the commit where a specific file was moved and merged. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
183. **You want to find the commit where a specific file was moved and rebased. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
184. **You want to find the commit where a specific file was moved and cherry-picked. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
185. **You want to find the commit where a specific file was moved and reverted. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
186. **You want to find the commit where a specific file was moved and amended. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
187. **You want to find the commit where a specific file was moved and squashed. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
188. **You want to find the commit where a specific file was moved and split. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
189. **You want to find the commit where a specific file was moved and filtered. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
190. **You want to find the commit where a specific file was moved and rewritten. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
191. **You want to find the commit where a specific file was moved and renamed. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
192. **You want to find the commit where a specific file was moved and modified. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
193. **You want to find the commit where a specific file was moved and deleted. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
194. **You want to find the commit where a specific file was moved and copied. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
195. **You want to find the commit where a specific file was moved and merged. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
196. **You want to find the commit where a specific file was moved and rebased. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
197. **You want to find the commit where a specific file was moved and cherry-picked. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
198. **You want to find the commit where a specific file was moved and reverted. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
199. **You want to find the commit where a specific file was moved and amended. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.
200. **You want to find the commit where a specific file was moved and squashed. How would you do it?**
     - **Answer:** Use `git log --follow <file_name>`.

---

Happy Learning😊!
