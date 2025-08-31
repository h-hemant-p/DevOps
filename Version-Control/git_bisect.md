## **Git Bisect**

*  `git bisect` helps **find the exact commit** that introduced a bug by performing a **binary search** through commit history.

* It systematically checks commits, dividing them into "good" and "bad" to locate the problematic change efficiently.

### **Basic Git Bisect Workflow**

1. **Start bisecting**

   ```sh
   git bisect start
   ```

   * Initializes the bisect process.
2. **Mark a known bad commit** (where the bug exists)

   ```sh
   git bisect bad <commit-hash>
   ```

   * Usually, this is the latest commit where the issue is observed.
3. **Mark a known good commit** (before the bug was introduced)

   ```sh
   git bisect good <commit-hash>
   ```

   * This should be a commit where everything worked fine.
4. **Git automatically checks out a middle commit**

   * Test if the bug exists at this point.
   * If the commit is  **bad** , run:
     ```sh
     git bisect bad
     ```
   * If the commit is  **good** , run:
     ```sh
     git bisect good
     ```
   * Git will continue bisecting until it finds the first bad commit.
5. **End the bisect session** (after finding the bad commit)

   ```sh
   git bisect reset
   ```

   * Resets back to the original branch.

---

### **Automating Bisect with a Script**

If you have a command that can detect the bug (e.g., a test script), you can automate `gi`

`t bisect`:

```sh
git bisect start
git bisect bad
git bisect good <commit-hash>
git bisect run ./test_script.sh
```

* Git will automatically check commits and stop when the faulty commit is found.

---

### **Example Workflow**

```sh
git bisect start
git bisect bad HEAD
git bisect good abc1234
```

* Git checks out a middle commit.
* Run tests manually, then mark as `good` or `bad`.
* Continue until Git identifies the first bad commit.
* Finish with:
  ```sh
  git bisect reset
  ```

---

### **When to Use `git bisect`?**

* When debugging **regressions** (finding which commit broke a feature).
* When investigating **unexpected behavior** introduced over multiple commits.
* When dealing with **large commit histories** where manually checking each commit is impractical.

Would you like a quick reference cheat sheet for this? 🚀
