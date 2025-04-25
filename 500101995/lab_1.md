# Devops Lab 1 - CI/CD Basics - Creating a GitHub Repository

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**  

---

## Overview
This guide walks through the basic steps to set up a GitHub repository, clone it locally, and add a README file as part of learning **CI/CD fundamentals**.

---

## **1. Create a GitHub Repository**
1. Go to [GitHub](https://github.com/).
2. Click on **New Repository**.
3. Provide a repository name (e.g., `ci-cd-demo`).
4. Select **Public** or **Private**.
5. Check **Add a README file** (optional).
6. Click **Create Repository**.

---

## **2. Clone the Repository Locally**
Open **Git Bash** or a terminal and run:
```bash
git clone https://github.com/<your-username>/ci-cd-demo.git
```
Navigate into the repository:
```bash
cd ci-cd-demo
```

---

## **3. Create a README.md File (If Not Already Present)**
If the repository does not contain a README file, create one:
```bash
touch README.md
```
Add initial content to the README file:
```bash
echo "# CI/CD Basics

This repository demonstrates the basics of CI/CD workflows." >> README.md
```

---

## **4. Stage, Commit, and Push the Changes**
Stage the README file:
```bash
git add README.md
```
Commit the file:
```bash
git commit -m "Added README.md"
```
Push changes to GitHub:
```bash
git push origin main
```

---

## **Key Learnings**
- How to **create a GitHub repository**.
- How to **clone a repository locally**.
- How to **add and commit a README file**.
- How to **push changes to GitHub**.

---
