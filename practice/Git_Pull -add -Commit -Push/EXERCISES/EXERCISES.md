# Git Practice: Init, Clone, Add, Commit, Push, Pull & Origin

This guide includes explanations and exercises to help you practice basic Git commands in a real workflow.

---

## 🧠 What is `git init`?

`git init` initializes a **new Git repository** in your local project folder. It creates a `.git/` directory where Git stores your commit history, config, and tracking information.

```bash
git init
```

---

## 🧠 What is `git clone`?

`git clone` downloads a **copy of a remote Git repository** (e.g., from GitHub) to your local machine. It also automatically sets up the remote as `origin`.

```bash
git clone https://github.com/username/repo.git
```

---

# 🧪 Practice Exercises

---

## 🧩 Exercise 1: Initialize a Local Repo and Push to GitHub

**Goal:** Create a new project and upload it to GitHub.

1. Create a project folder:
   ```bash
   mkdir git-practice
   cd git-practice
   ```

2. Initialize Git:
   ```bash
   git init
   ```

3. Create a file:
   ```bash
   echo "# Git Practice" > README.md
   ```

4. Stage and commit:
   ```bash
   git add README.md
   git commit -m "Initial commit"
   ```

5. Create a new empty repo on GitHub, then connect it:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/git-practice.git
   git branch -M main
   git push -u origin main
   ```

---

## 🧩 Exercise 2: Make Changes and Push Again

1. Add a new file:
   ```bash
   echo "print('Hello Git!')" > hello.py
   ```

2. Add and commit:
   ```bash
   git add hello.py
   git commit -m "Add hello.py"
   git push origin main
   ```

---

## 🧩 Exercise 3: Pull Remote Changes

1. Edit `README.md` directly on GitHub (e.g., add a new line).

2. Then pull the change into your local repo:
   ```bash
   git pull origin main
   ```

---

## 🧩 Exercise 5: Change the Remote Origin

1. Create a new repo on GitHub.

2. Change the remote in your local project:
   ```bash
   git remote set-url origin https://github.com/YOUR_USERNAME/new-repo.git
   git push -u origin main
   ```

---

## 💡 Summary of Commands

| Command                     | Description                                 |
|----------------------------|---------------------------------------------|
| `git init`                 | Initialize a local Git repo                 |
| `git clone <url>`          | Clone a remote repository                   |
| `git add .`                | Stage all changes                           |
| `git commit -m "msg"`      | Save changes locally                        |
| `git push origin main`     | Upload changes to the remote repo           |
| `git pull origin main`     | Download and merge changes from remote      |
| `git remote -v`            | Show linked remote repositories             |

---
