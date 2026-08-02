# 📘 Module 3 - Jenkins Installation

## 📖 Overview

In this module, I learned how Jenkins works internally and installed Jenkins on an Ubuntu EC2 instance. I also understood why Java is required, how the Jenkins Controller and Agents work, and completed the initial Jenkins setup.

---

# 📚 Topics Covered

## ✅ Jenkins Architecture

- What is Jenkins Architecture?
- Components of Jenkins
- How Jenkins works internally

---

## ✅ Jenkins Controller (Master)

- Role of the Controller
- Scheduling Jobs
- Managing Plugins
- Managing Users
- Assigning Jobs to Agents

---

## ✅ Jenkins Agent (Node)

- What is an Agent?
- Why Agents are required
- Distributed Builds
- Scalability
- Performance Benefits

---

## ✅ Java Basics

- What is Java?
- Why Jenkins needs Java
- JDK vs JRE
- Verify Java Installation

Commands Used:

```bash
java -version
javac -version
which java
```

---

## ✅ Jenkins System Requirements

- CPU
- RAM
- Storage
- Supported Operating Systems
- Port 8080
- Why Linux is preferred

---

## ✅ Installing Java

Commands:

```bash
sudo apt update
sudo apt install openjdk-21-jdk -y
java -version
javac -version
```

---

## ✅ Installing Jenkins

Commands:

```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins -y

sudo systemctl start jenkins

sudo systemctl enable jenkins

sudo systemctl status jenkins
```

---

## ✅ Access Jenkins

Open in browser:

```
http://<EC2-Public-IP>:8080
```

Unlock Jenkins:

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

---

## 📸 Screenshots

- Java Installation
- Jenkins Installation
- Jenkins Service Status
- Jenkins Login Page
- Jenkins Dashboard
- EC2 Instance
- Security Group (Port 8080)

---

## ⚠️ Troubleshooting

### Repository Not Signed Error

Issue:

```
The repository 'https://pkg.jenkins.io/debian-stable binary/ Release' is not signed.
```

Resolution:

- Verified the Jenkins repository configuration.
- Re-added the official Jenkins GPG key.
- Updated the package list.
- Confirmed Jenkins service was running successfully.

---

### Jenkins Not Accessible

Possible Causes:

- Port 8080 blocked
- Jenkins service stopped
- Security Group misconfigured

Commands Used:

```bash
sudo systemctl status jenkins
sudo ss -tulnp | grep 8080
```

---

# 🎯 Key Learnings

- Understood Jenkins Architecture.
- Learned the role of Controller and Agents.
- Installed Java successfully.
- Installed Jenkins on Ubuntu.
- Configured Jenkins as a system service.
- Accessed Jenkins using the browser.
- Solved a real-world repository signing issue.

---

# 📝 Interview Questions

1. Why does Jenkins require Java?
2. What is the difference between JDK and JRE?
3. What is the Jenkins Controller?
4. What is a Jenkins Agent?
5. Why do companies use multiple Agents?
6. Which port does Jenkins use by default?
7. How do you start the Jenkins service?
8. How do you check the Jenkins service status?
9. How do you unlock Jenkins?
10. Explain the Jenkins installation process.

---

# 🚀 Status

✅ Module 3 Completed
