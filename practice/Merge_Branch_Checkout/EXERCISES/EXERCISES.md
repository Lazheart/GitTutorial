# Git Practice Exercises: Branching, Merging, Conflicts, Checkout & Fetch

These exercises will help you get hands-on experience with essential Git branching and collaboration concepts.

---

## 🧩 Exercise 1: Create and Switch Between Branches

1. Clone your practice repo or create a new one:
   ```bash
   git clone https://github.com/YOUR_USERNAME/git-practice.git
   cd git-practice
   ```

2. Create a new branch:

   ```bash
   git branch feature-1
   ```

3. Switch to it and create a file:

   ```bash
   git checkout feature-1
   echo "Feature 1 work" > feature.txt
   git add .
   git commit -m "Add feature 1 file"
   ```

4. Switch back to main:

   ```bash
   git checkout main
   ```

---

## 🧩 Exercise 2: Merge a Branch

1. Merge the feature branch into main:

   ```bash
   git merge feature-1
   ```

2. Push the changes:

   ```bash
   git push origin main
   ```

---

## 🧩 Exercise 3: Simulate a Merge Conflict

1. In `main` branch, edit `README.md` and commit:

   ```bash
   echo "Main branch change" >> README.md
   git add .
   git commit -m "Edit README from main"
   ```

2. Create a new branch:

   ```bash
   git checkout -b conflict-test
   ```

3. Edit the **same lines** in `README.md`, then commit:

   ```bash
   echo "Conflict branch change" >> README.md
   git add .
   git commit -m "Edit README from conflict-test"
   ```

4. Switch back to `main` and try to merge:

   ```bash
   git checkout main
   git merge conflict-test
   ```

5. Git will report a conflict. Open the file and fix it manually by choosing what to keep.

6. After fixing, complete the merge:

   ```bash
   git add README.md
   git commit -m "Resolve conflict in README.md"
   ```

---

## 🧩 Exercise 4: Use `git fetch` and Merge

1. On GitHub, edit a file in `main` (e.g., add a line to `README.md`).

2. In your local repo, run:

   ```bash
   git fetch origin
   ```

3. Check the differences (optional):

   ```bash
   git diff origin/main
   ```

4. Merge the changes manually:

   ```bash
   git merge origin/main
   ```

---

## 🧩 Exercise 5: Restore a File with Checkout

1. Edit a file (e.g., `feature.txt`) without committing.

2. Restore it to the last committed version:

   ```bash
   git checkout -- feature.txt
   ```

This will discard local changes and revert the file.

---

## ✅ Recap

| Exercise | Concept Covered              |
| -------- | ---------------------------- |
| 1        | Branch creation & switching  |
| 2        | Merging branches             |
| 3        | Merge conflicts & resolution |
| 4        | Fetching and manual merge    |
| 5        | File recovery with checkout  |

---
