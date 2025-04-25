# DevOps Lab 3 - Git Basics & Usage Guide

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**  

---

## Overview
In this lab session, we learned the fundamentals of **Git**, including how to configure Git, initialize repositories, manage commits, and work with remote repositories.

## Steps to Set Up Git and Use It Effectively

### 1. Git Setup
Before using Git, configure your user details:
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

---

### 2. Initialize a Repository
Create a new Git repository:
```bash
git init
```

Clone an existing repository:
```bash
git clone <repository_url>
```

---

### 3. Check Repository Status
To check the current status of the repository:
```bash
git status
```

---

### 4. Adding & Committing Changes
Stage specific files:
```bash
git add <file_name>
```

Stage all files:
```bash
git add .
```

Commit changes:
```bash
git commit -m "Your commit message"
```

---

### 5. Viewing History
Check commit history:
```bash
git log
```

Shortened history:
```bash
git log --oneline
```

---

### 6. Pushing & Pulling Changes
Push local changes to the remote repository:
```bash
git push origin <branch_name>
```

Pull the latest changes:
```bash
git pull origin <branch_name>
```

---

### 7. Setting Up SSH for Git
Using SSH instead of HTTPS for Git authentication provides better security and ease of use.

#### **Step 1: Generate an SSH Key**
```bash
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
```
Press **Enter** to save the key in the default location, then set a passphrase if needed.

#### **Step 2: Start the SSH Agent and Add Your Key**
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

#### **Step 3: Add the SSH Key to GitHub**
Copy your SSH key:
```bash
cat ~/.ssh/id_rsa.pub
```
Go to **GitHub → Settings → SSH and GPG keys → New SSH Key**, and paste your key.

#### **Step 4: Test SSH Connection**
```bash
ssh -T git@github.com
```
If successful, you'll see a message: *"Hi <your-username>! You've successfully authenticated."*

#### **Step 5: Use SSH for Git Operations**
Instead of HTTPS, use SSH URLs when cloning repositories:
```bash
git clone git@github.com:<username>/<repository>.git
```

---

### 8. Installation
To get started, clone this repository:
```bash
git clone <repository_url>
cd repository-name
```

---

### 9. Contribution Guidelines
Want to contribute? Follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Added a new feature"
   ```
4. Push the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a Pull Request.

---

## Key Learnings
- How to **configure Git** with user details.
- How to **initialize and clone repositories**.
- How to **check repository status and commit changes**.
- How to **view commit history and track changes**.
- How to **push and pull changes from remote repositories**.
- How to **set up SSH authentication for Git**.
- How to **contribute to open-source projects using Git**.

---
