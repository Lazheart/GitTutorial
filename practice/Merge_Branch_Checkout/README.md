# Git Concepts: Branching, Merge, Conflicts, Checkout & Fetch

This document explains key Git concepts often used in collaborative workflows and version control.

---

## 🌿 What is a Git Branch?

A **branch** is a lightweight, movable pointer to a commit. It allows you to work on new features or fixes **without affecting the main codebase**.

```bash
git branch new-feature     # create a new branch
git checkout new-feature   # switch to that branch
```

Common practice:
- `main` or `master` → production code
- `feature/*`, `bugfix/*` → work in progress

---

## 🔀 What is `git merge`?

`git merge` combines the history of two branches. It’s typically used to **integrate a feature branch into the main branch**.

```bash
git checkout main
git merge new-feature
```

This creates a new merge commit if there are changes in both branches.

---

## ⚠️ What is a Merge Conflict?

A **merge conflict** occurs when Git can’t automatically reconcile differences between branches (e.g., changes to the same line of a file).

You’ll see conflict markers like this in your files:

```text
<<<<<<< HEAD
Current change
=======
Incoming change
>>>>>>> new-feature
```

To fix it:
1. Manually edit the file to keep what you want.
2. Stage the file:
   ```bash
   git add <filename>
   ```
3. Commit the resolution:
   ```bash
   git commit -m "Resolve merge conflict"
   ```

---

## 🧭 What is `git checkout`?

`git checkout` is used to switch between branches or restore files.

```bash
git checkout main         # switch to main branch
git checkout -b test-1    # create and switch to a new branch
```

You can also use it to discard local changes:
```bash
git checkout -- file.txt  # restore file to last committed version
```

---

## ⬇️ What is `git fetch`?

`git fetch` downloads changes from a remote repository but **does NOT merge them** into your local branch.

```bash
git fetch origin
```

This updates your remote tracking branches (like `origin/main`), so you can review changes before merging.

To manually apply the updates:

```bash
git merge origin/main
```

This is safer than `git pull` because you get a chance to review changes before merging.

---

## ✅ Summary Table

| Command                          | Description                                   |
|----------------------------------|-----------------------------------------------|
| `git branch <name>`              | Create a new branch                           |
| `git checkout <name>`            | Switch to a branch                            |
| `git checkout -b <name>`         | Create and switch to a new branch             |
| `git merge <branch>`             | Merge changes from another branch             |
| `git fetch`                      | Download changes from remote (no merge)       |
| `git merge origin/main`         | Merge fetched changes into local branch       |
| _Conflict resolution_            | Manually fix conflict, then `add` and `commit`|

---

Understanding these concepts helps you work with teams, manage multiple features, and safely control your code changes.

Happy branching! 🌱
