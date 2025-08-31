## Introduction

Git is a **distributed version control system (DVCS)** that helps developers track changes in code, collaborate efficiently, and manage project history. It was created by **Linus Torvalds** in 2005 for Linux kernel development but is now widely used across software projects.

##### **Key Features of Git**

* **Distributed System** → Every developer has a complete copy of the repository.
* **Version Control** → Tracks changes, allowing rollback to previous versions.
* **Branching and Merging** → Enables parallel development and easy integration.
* **Speed & Efficiency** → Optimized for performance, even in large projects.
* **Collaboration** → Supports multiple developers working on the same project.

##### **Basic Git Commands**

* Set Global Username and Email

```bash
git config --global user.name "<your username>"  
git config --global user.email "<your email>"  
```

* **Initialize an folder**

```bash
git init
```

* **Clone a Repository**

```bash
git clone <repo-url>
```

* **Check Repository Status**

```bash
git status
```

* **Stage Changes(add to commit)**

```bash
git add <file>
```

* **Commit Changes**

```bash
git commit -m "Descriptive commit message"
```

* **Push Changes to Remote Repository**

```bash
git push origin <branch>
```

* **Pull Updates from Remote Repository**

```bash
git pull origin <branch>
```

* **Add a remote repository:**

```bash
git remote add origin <repo-url>
```

* **List remote repositories(show remote origin url):**

```bash
git remote -v
```

* **Fetch remote changes without merging:**

```bash
git fetch origin
```

* **Undo last commit (keep changes unstaged):**

```bash
git reset --soft HEAD~1
```

* **Undo last commit (remove changes completely):**

```bash
git reset --hard HEAD~1
```

* **Discard unstaged changes in a file:**

```bash
git checkout -- <file>
```

* **Show Branches in Your Repository**

```bash
git branch  
```

* **Create a new branch:**

```bash
git branch <branch_name>
```

* **Switch to the another branch:**

```bash
git checkout <branch_name>
```

* **Create a new branch and Switch to that branch:**

```bash
git checkout -b <branch_name>
```

* **Remove a Branch from Git**

```bash
git branch -d <branch name>  
```

* **Check Git Commits and Logs**

```bash
git log  
```

* **Restore File from Being Modified to Tracked**

```bash
git restore <filename>  
git checkout <filename>  
```
