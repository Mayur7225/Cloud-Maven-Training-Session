# Practical 01 – Git Installation, Configuration & First Repository

**Name:** Mayur Aware

## Objective

The objective of this task is to install Git, configure user identity, create a repository, and make the first commit.

---

# Step 1 – Install Git

Git was installed on the Ubuntu system and verified using the following command:

```
git --version
```

This command confirms that Git is successfully installed.

Screenshot:

![Git Version](screenshots/git-version.png)

---

# Step 2 – Configure Git Identity

Global Git username and email were configured using:

```
git config --global user.name "Mayur Aware"
git config --global user.email "your-email@example.com"
```

These settings define the author information for commits.

---

# Step 3 – Create Repository

A new directory called `git-nginx-assessment` was created and initialized as a Git repository.

```
mkdir git-nginx-assessment
cd git-nginx-assessment
git init
```

---

# Step 4 – Create Project Files

Two files were created.

**README.md**

```
# Git NGINX Assessment
Mayur Aware
```

**app.py**

```
print("Hello Git")
```

---

# Step 5 – Stage and Commit Files

The files were staged and committed using:

```
git add README.md app.py
git commit -m "Initial commit: add README and app.py"
```

This created the first commit in the repository.

---

# Step 6 – View Commit History

To view commit history the following command was used:

```
git log
```

This command shows commit hash, author name, date, and commit message.

Screenshot:

![Git Log](screenshots/git-log.png)

---

# Commands Used

```
git --version
git config --global user.name
git config --global user.email
git init
git add
git commit
git log
```

---

# Conclusion

In this practical we installed Git, configured user identity, created a repository, added project files, and made the first commit successfully.

