# DevOps Lab 5 - Learning Git Submodules

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**

---

## Overview
In this lab session, we learned about **Git submodules**, how to add them to a repository, and how to manage them effectively.

## Steps to Work with Git Submodules

### 1. Initialize a New Git Repository
```sh
echo "# demo-main" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/gurmehr04/demo-main.git
git push -u origin main
```

### 2. Add a New File and Commit Changes
```sh
git status
git add .
git commit -m "index"
git push
```

### 3. Add Git Submodules
Adding a CSS submodule:
```sh
git submodule add https://github.com/gurmehr04/demo-css.git
```

Adding a JavaScript submodule:
```sh
git submodule add https://github.com/gurmehr04/demo-js.git
```

### 4. Commit and Push Submodules
```sh
git commit -m "submodules"
git push
```

---

## Key Learnings
- How to **initialize a Git repository**.
- How to **add and commit files** to a repository.
- How to **add Git submodules** to manage dependencies.
- How to **commit and push submodule changes**.
- Understanding the role of **`.gitmodules`** in submodule management.

---
<!-- ---

## Reference Repository:
[Demo Main Repository](https://github.com/gurmehr04/demo-main) -->
