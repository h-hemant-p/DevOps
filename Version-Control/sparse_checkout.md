## Git Sparse Checkout

Git **sparse checkout** allows you to clone a repository but check out only specific directories or files instead of the entire repo. This is useful for working with large repositories where you don't need all files.

* **Enable Sparse Checkout**

```bash
git sparse-checkout init  
```

* **Specify the files or directories to check out**

```bash
git sparse-checkout set path/to/directory path/to/file
# Example
git sparse-checkout set src docs
# This checks out only the `src` and `docs` folders.
```

* **Clone a repository with sparse checkout (optional)**

```bash
git clone --filter=blob:none --no-checkout <repo-url>
cd <repo-name>
git sparse-checkout init
git sparse-checkout set path/to/directory
git checkout main  # or any branch you need
```

* **Check the current sparse checkout list**

```bash
git sparse-checkout list
```

* **Add more files/folders to sparse checkout**

```sh
git sparse-checkout add new/path/to/include
```

* **Disable Sparse Checkout (Get the entire repo back)**

```sh
git sparse-checkout disable
```

---

#### **Example Use Case**

1. Clone a large monorepo without checking out all files:
   ```sh
   git clone --filter=blob:none --no-checkout https://github.com/example/large-repo.git
   cd large-repo
   ```
2. Enable sparse checkout and fetch only the `frontend` and `backend` directories:
   ```sh
   git sparse-checkout init
   git sparse-checkout set frontend backend
   git checkout main
   ```
3. If you later need the `config` directory as well:
   ```sh
   git sparse-checkout add config
   ```
