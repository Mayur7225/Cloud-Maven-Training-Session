# Practical 3 - Git Stash, Revert, Reset and Amend

In this practical we performed different Git operations related to stash, undoing commits and modifying commit history.

---

## 3a. Git Stash

First we modified the `app.py` file by adding a comment.

Then we checked the status:
git status

After that we saved the changes temporarily using:
git stash

Now the working directory became clean.

To restore the changes back we used:
git stash pop


This command brought back the previously stashed changes.

---

## 3b. Git Revert

We created a new file called `bug.txt` with the content:


This is a bug
Then we committed the file:


git add bug.txt
git commit -m "add bug file"


To undo this commit safely we used:


git revert HEAD


This created a new commit which reverses the previous change.

To verify we used:


git log --oneline


---

## 3c. Git Commit Amend

We created a file called `hotfix.txt` and committed it.


git add hotfix.txt
git commit -m "hotfix"


Later we updated the commit message using:


git commit --amend -m "fix: hotfix with corrected message"


This modifies the most recent commit message.

---

## 3d. Git Reset (Soft)

We created two commits and then used the following command:


git reset --soft HEAD~1


This removed the last commit but kept the changes staged.

We confirmed this using:


git status


---

## Commands Used


git stash
git stash pop
git revert
git commit --amend
git reset --soft
git log --oneline


---

## Conclusion

In this practical we learned how to temporarily save changes using stash, undo commits using revert, modify commit messages using amend, and manage commit history using reset.
