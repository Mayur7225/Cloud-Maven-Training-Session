# Practical 4 – Git Branching and Merge Conflict

## Objective

The objective of this task is to understand how Git branches work and how merge conflicts occur and are resolved.

---

## Step 1 – Create a Feature Branch

A new branch was created to simulate feature development.

Command used:

git checkout -b feature/conflict-demo

---

## Step 2 – Add File in Feature Branch

A file named `conflict.txt` was created and committed in the feature branch.

Commands:

git add conflict.txt
git commit -m "Add conflict file from feature branch"

---

## Step 3 – Modify File in Main Branch

The same file was modified in the `main` branch with different content.

Commands:

git checkout main
git add conflict.txt
git commit -m "Update conflict file from main branch"

---

## Step 4 – Merge Branch

When merging the feature branch into the main branch, Git detected a merge conflict.

Command:

git merge feature/conflict-demo

Git displayed conflict markers inside the file.

---

## Step 5 – Resolve Conflict

The conflict was manually resolved by editing the file and removing the conflict markers.

Commands used:

git add conflict.txt
git commit -m "Resolve merge conflict"

---

## Screenshot

Below is the screenshot showing the merge conflict process.

![Merge Conflict Screenshot](Practical 4.png)

---

## Commands Used

git branch
git checkout
git merge
git add
git commit
git log --oneline

---

## Conclusion

In this task we learned how Git detects merge conflicts when the same file is modified in multiple branches and how developers resolve these conflicts manually.

