
# DevOps Lab 4 - GIT Branching, Merge, Rebase
 

## Author

**Gurmehr Singh Gulati**

**500101995**

**R2142220078**

**Full Stack AI B1-Hons**

---

## Overview
In this lab session, we learned how to create and manage Git repositories, manipulate files, and track changes using various Git commands. 

## Steps Performed

### 1. Creating a Project Directory
```bash
mkdir project   # Create project directory
cd project      # Navigate into the project directory
mkdir src       # Create src directory
ls              # List directory contents
```

---

### 2. Creating and Modifying a README.md File
```bash
touch README.md           # Create README.md file
ls                        # Verify file creation
cat README.md             # Check contents (empty initially)
echo "Hello World" >> README.md  # Append text to README.md
cat README.md             # Display file contents
```

Handling Escape Sequences in Echo:
```bash
echo "hello \n me"       # Prints \n as text
echo -e "hello \n me"   # Properly interprets new line
```

Overwriting File Contents:
```bash
echo "Hello World 1" > README.md  # Overwrites file
echo "content" >> README.md && cat README.md  # Append & display
```

---

### 3. Initializing a Git Repository
```bash
git init                 # Initialize Git repository
git remote -v           # Check for remote repositories
git branch              # List branches
git status              # Check repository status
```

---

### 4. Staging and Committing Files
```bash
git add .                      # Stage all files
git commit -m "Initial commit" # Commit changes
git status                     # Verify clean working directory
```

---

### 5. Renaming the Default Branch
```bash
git branch -M main  # Rename master to main
git branch          # Verify branch name
```

---

### 6. Viewing and Managing Commit History
```bash
git log                        # View commit history
git reset --soft <commit_id>  # Undo the latest commit (keeps changes)
git checkout <commit_id>       # Switch to an older commit
```

---

### 7. Working with Branches
```bash
git branch featureA       # Create a new branch
git checkout featureA     # Switch to featureA
```

Adding and Committing Changes:
```bash
touch z.txt
git add . && git commit -m "Added z.txt"

touch x.txt
git add . && git commit -m "Added x.txt"
```

Switching Between Branches:
```bash
git checkout main    # Switch back to main
git checkout featureA  # Switch back to featureA
```

---

### 8. Rebasing and Merging
```bash
git rebase main     # Reapply featureA changes onto main
git branch featureB # Create featureB from featureA
git merge featureB  # Merge featureB into main
```

---

### 9. Resetting and Squashing Commits
```bash
git reset --hard <commit_id>  # Reset repo to an earlier state
git merge --squash featureB   # Squash merge featureB into main
git commit -m "Squashed changes"
```

---

## Key Learnings
- How to **initialize a Git repository** and manage branches.
- How to **create, modify, and track files** in Git.
- How to **reset commits and work with branch history**.
- How to **merge, rebase, and squash commits**.
- Understanding Git's **branching model and workflow**.

---
