
# Devops Lab 2 - Installing WSL, Ubuntu, and Docker Desktop

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**  

---

## Overview
This guide will walk you through installing **Windows Subsystem for Linux (WSL)**, setting up **Ubuntu**, and installing **Docker Desktop** to enable containerized development on a Windows system.

---

## **1. Installing Windows Subsystem for Linux (WSL)**
WSL allows you to run a Linux environment directly on Windows without the need for a virtual machine.

### **Step 1: Enable WSL**
Open **PowerShell as Administrator** and run:
```powershell
wsl --install
```
This will install the latest WSL version along with Ubuntu as the default distribution.

If WSL is already installed, update it with:
```powershell
wsl --update
```

### **Step 2: Check Installed WSL Versions**
To verify that WSL is installed:
```powershell
wsl -l -v
```

---

## **2. Installing Ubuntu on WSL**
If Ubuntu was not installed automatically, you can manually install it.

### **Step 1: Install Ubuntu**
Download and install Ubuntu from the **Microsoft Store**:
1. Open the **Microsoft Store**.
2. Search for **Ubuntu**.
3. Click **Install**.

Alternatively, install it using PowerShell:
```powershell
wsl --install -d Ubuntu
```

### **Step 2: Set Up Ubuntu**
Once installed, launch Ubuntu from the Start Menu and complete the setup:
```sh
wsl
```
Create a user and password when prompted.

---

## **3. Installing Docker Desktop on Windows**
Docker Desktop provides an easy-to-use interface for managing containers on Windows.

### **Step 1: Download Docker Desktop**
Download the latest version of Docker Desktop from the official Docker website:
[Download Docker Desktop](https://www.docker.com/products/docker-desktop/)

### **Step 2: Install Docker Desktop**
1. Run the downloaded **Docker Desktop Installer**.
2. Follow the installation instructions.
3. Ensure **WSL 2 backend** is selected during installation.

### **Step 3: Start Docker Desktop**
1. Open **Docker Desktop** from the Start Menu.
2. Wait for the Docker Engine to start.
3. Verify installation by running:
```powershell
docker --version
docker run hello-world
```

If Docker runs successfully, you have completed the installation.

---

## **Key Learnings**
- Installed **WSL** and verified it using PowerShell.
- Installed **Ubuntu** and completed initial setup.
- Installed **Docker Desktop** and configured it to use WSL 2.
- Verified Docker installation and ran a test container.

---
