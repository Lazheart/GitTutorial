# Git Basics: Add, Commit, Push , Pull & Origin

This guide explains the basic Git commands used to upload your local code to a remote repository, such as GitHub.

---

## 🔹 1. `git add`

Adds your file changes to the **staging area**. This means you’re telling Git: “I want to include these changes in the next commit.”

```bash
git add <filename>   # Add a specific file
git add .            # Add all changes in the current directory
```

---

## 🔹 2. `git commit`

Saves a snapshot of your staged changes to the local repository. A commit represents a checkpoint in your project history.

```bash
git commit -m "Your descriptive message here"
```

✅ Tip: Always use clear and meaningful commit messages to describe what you changed.

---

## 🔹 3. `git push`

Uploads your **local commits** to the **remote repository** (e.g., GitHub).

```bash
git push origin main
```

- `origin` → the name of the remote repository
- `main` → the name of the branch you’re pushing to

---

## 🔹 4. What is `origin`?

`origin` is the **default alias** Git uses for the remote repository URL you cloned from or set manually.

You can check the remote like this:

```bash
git remote -v
```

Example output:

```
origin  https://github.com/yourusername/your-repo.git (fetch)
origin  https://github.com/yourusername/your-repo.git (push)
```

So when you run `git push origin main`, you're saying:
> “Send my commits to the `main` branch of the remote called `origin`.”


---

## 🔄 5. `git pull`

The `git pull` command is used to **update your local repository** with the latest changes from the **remote repository**.

It’s like saying:
> “Bring me the latest version of the project from GitHub (or the remote) and merge it into my local copy.”

### 📌 Syntax

```bash
git pull origin main
```

- `origin` → the remote repository you want to pull from.
- `main` → the branch you want to update from.

### 🧠 What does `git pull` do?

Under the hood, `git pull` does two things:
1. `git fetch` – downloads the latest commits from the remote.
2. `git merge` – merges those commits into your current branch.

### ⚠️ Why is it important?

You should always pull **before pushing**, especially if you're working in a team or from multiple devices. This avoids merge conflicts and keeps your codebase up-to-date.

---

### ✅ Example workflow

```bash
git pull origin main
# check the changes, fix conflicts if any
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

---

## 🛠 Typical Workflow

```bash
git add .
git commit -m "Write a meaningful message"
git push origin main
```

This sequence will stage your changes, commit them locally, and push them to GitHub (or another Git server).

---

## 🔐 Optional: GitHub Setup

### 1. Clone a repository

```bash
git clone https://github.com/username/repository.git
```

### 2. Connect an existing local project to GitHub

```bash
git remote add origin https://github.com/username/repository.git
git branch -M main
git push -u origin main
```

> Replace the URL with your actual GitHub repo URL.

---

## ⚠️ Common Tips

- Always **pull before pushing** to avoid conflicts:
  ```bash
  git pull origin main
  ```
---

## 📚 Learn More

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/en/get-started)

---
