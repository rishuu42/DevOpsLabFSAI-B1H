# DevOps Lab 7 - Git Forking and Open Source Contribution

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**

---

## Overview
This document explains the steps followed to fork a repository, clone it, and contribute by adding a folder and a `README.md` file.

## Steps

### 1. Forking the Repository
Forked the repository on GitHub from `gurmehr04/DevOpsLabFSAI-B1H`.

### 2. Cloning the Forked Repository
```sh
git clone https://github.com/gurmehr04/DevOpsLabFSAI-B1H.git
```

### 3. Creating a New Folder with SAP ID
```sh
mkdir 500101995
cd 500101995
```

### 4. Creating a README File
```sh
touch readme.md
echo "Hi! My name is Gurmehr Singh Gulati and my SAP ID is 500101995" >> readme.md
```

### 5. Adding and Committing the Changes
```sh
git add .
git commit -m "readme file"
```

### 6. Pushing Changes to the Remote Repository
Attempted to push changes, but encountered an issue:
```sh
git push
```
Error:
```
fatal: No configured push destination.
```
Resolved by setting upstream branch:
```sh
git push --set-upstream https://github.com/gurmehr04/DevOpsLabFSAI-B1H.git main
```

### 7. Final Push and Verification
```sh
git push
```
Successfully pushed the changes to the repository.

---

## Key Learnings
- How to **fork a repository** on GitHub.
- How to **clone a repository** to a local system.
- Creating and **managing files** inside a cloned repository.
- How to **commit and push** changes to a remote repository.
- Understanding **Git errors and resolutions** related to remote branches.

---

### Reference Repository:
[DevOpsLabFSAI-B1H](https://github.com/gurmehr04/DevOpsLabFSAI-B1H)

---