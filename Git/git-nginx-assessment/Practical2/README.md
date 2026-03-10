# Practical 02 – Branching, Committing & Pull Request Workflow

**Name:** Mayur Aware

## Objective

The objective of this task is to understand Git branching workflow, making commits in a feature branch, and creating a Pull Request on GitHub.

---

# Step 1 – Create a Feature Branch

From the main branch a new feature branch was created following Git naming best practices.

Command used:

git checkout -b feature/add-calculator

This command creates and switches to a new branch.

Screenshot:

![Create Branch](screenshots/create-branch.png)

---

# Step 2 – Add Calculator File

A new file named `calculator.py` was created containing Python functions.

Example code:

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

The file was staged and committed.

Commands used:

git add calculator.py
git commit -m "Add calculator module with add and subtract functions"

---

# Step 3 – Update README

The README file was updated to mention the newly added calculator module.

Commands:

git add README.md
git commit -m "Update README to include calculator module"

---

# Step 4 – Push Feature Branch

The feature branch was pushed to GitHub.

Command used:

git push origin feature/add-calculator

---

# Step 5 – Create Pull Request

On GitHub a Pull Request was created from:

feature/add-calculator → main

The PR page showed the list of commits and file differences.

Screenshot:

![Pull Request Page](screenshots/pull-request.png)

---

# Step 6 – Merge Pull Request

The Pull Request was merged into the main branch on GitHub.

After merging, the local repository was updated using:

git checkout main
git pull origin main

---

# Commands Used

git branch
git checkout -b
git add
git commit
git push
git merge
git pull

---

# Conclusion

In this practical we learned how to create a feature branch, add new code, commit changes, push the branch to GitHub, and merge the changes using a Pull Request workflow.

