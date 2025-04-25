# DevOps Lab 8

## Name: Rishitt Gupta 
**SAP ID:** 500107002  
**Roll Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

## Jenkins - CI/CD Automation  

---

### **1. Install Jenkins on Ubuntu (WSL or Virtual Machine)**

#### a. Update package list and install Java (required by Jenkins):
```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
```

#### b. Add Jenkins repository key

#### c. Install Jenkins:
```bash
sudo apt update
sudo apt install jenkins -y
```

---

### **2. Start Jenkins service**
```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

---

### **3. Access Jenkins on browser**  
Open your browser and go to:  
[http://localhost:8080](http://localhost:8080)

---

### **4. Unlock Jenkins**
Use the following command to retrieve the initial admin password:
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Paste this password into the Jenkins web interface to continue setup.

---

### **5. Install Suggested Plugins**
- Choose **Install suggested plugins** when prompted.
- Wait for the installation to complete.
- Create your first admin user (username, password, full name, email).

---

### **6. Create a Freestyle Project**

1. Click on **New Item**
2. Enter **MyFirstJob** as project name
3. Select **Freestyle project** → Click **OK**
4. Go to the **Build** section → Click **Add build step** → Choose **Execute shell**
5. Enter the following script:
   ```bash
   echo "Hello from Jenkins"
   ```

---

### **7. Build the Job**

- Click **Build Now**
- Check the output in **Console Output**

---

### **8. Configure GitHub Webhook (Optional)**

1. In your GitHub repo:
   - Go to **Settings → Webhooks → Add Webhook**
   - Payload URL: `http://<your-jenkins-ip>:8080/github-webhook/`
   - Content type: `application/json`
   - Choose: **Just the push event**
   - Click **Add webhook**

2. In Jenkins:
   - Go to **MyFirstJob → Configure**
   - Under **Build Triggers**, check **GitHub hook trigger for GITScm polling**

---

### **9. Done**

You have now successfully installed Jenkins, created a freestyle job, and optionally configured a GitHub webhook for automation.