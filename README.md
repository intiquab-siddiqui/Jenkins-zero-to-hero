
# 🚀 Jenkins Zero to Hero

Welcome to my **Jenkins Zero to Hero** learning repository!

This repository documents my journey of learning **Jenkins from beginner to advanced** through theory, hands-on practice, troubleshooting, interview preparation, and real-world CI/CD concepts.

My goal is not just to learn Jenkins theoretically, but to build practical DevOps skills and create a portfolio that demonstrates my hands-on learning to recruiters and hiring managers.

---

# 👨‍💻 About Me

Hi, I'm **Intiquab Siddiqui**.

I am currently learning **DevOps** with a strong focus on practical, hands-on experience.

This repository is part of my DevOps learning journey, where I document what I learn step by step, practice concepts on AWS EC2, troubleshoot real issues, and build Jenkins-based CI/CD workflows.

---

# 🎯 Repository Goal

This repository is designed to help me:

* Learn Jenkins from scratch
* Understand CI/CD concepts
* Practice Jenkins administration
* Create and manage Jenkins jobs
* Integrate Jenkins with Git and GitHub
* Understand Jenkins workspaces and build processes
* Practice troubleshooting
* Prepare for Jenkins and DevOps interviews
* Build real-world CI/CD projects
* Document my learning journey

---

# 🛠️ Technologies & Tools Used

* **Jenkins**
* **Git**
* **GitHub**
* **Ubuntu Linux**
* **AWS EC2**
* **Java / OpenJDK**
* **Shell Commands**
* **CI/CD Concepts**

---

# 📚 Course Progress

| Module      | Topic                        | Status             |
| ----------- | ---------------------------- | ------------------ |
| ✅ Module 1  | Introduction to Jenkins      | Completed          |
| ✅ Module 2  | CI/CD Fundamentals           | Completed          |
| ✅ Module 3  | Jenkins Installation         | Completed          |
| ✅ Module 4  | Jenkins Dashboard            | Completed          |
| ✅ Module 5  | Jenkins Freestyle Jobs       | Completed          |
| ✅ Module 6  | Jenkins + GitHub Integration | Completed          |
| 🔄 Module 7 | Jenkins Pipelines            | In Progress / Next |
| ⏳ Module 8  | Docker Integration           | Coming Soon        |
| ⏳ Module 9  | Jenkins Agents               | Coming Soon        |
| ⏳ Module 10 | Real-World CI/CD Project     | Coming Soon        |

> This roadmap will be updated as I progress through the course.

---

# 📁 Repository Structure

```text
Jenkins-zero-to-hero/
│
├── README.md
│
├── Module-01-Introduction/
│   └── README.md
│
├── Module-02-CI-CD/
│   └── README.md
│
├── Module-03-Installation/
│   └── README.md
│
├── Module-04-Dashboard/
│   └── README.md
│
├── Module-05-Freestyle-Jobs/
│   └── README.md
│
├── module-06-Jenkins-Github-Integration/
│   └── README.md
│
├── handwritten-notes/
│
└── screenshots/
```

---

# 📖 What You'll Find

Each module is designed to contain practical learning material such as:

* 📚 Theory Notes
* 💻 Hands-on Practice
* 📝 Handwritten Notes
* 📸 Screenshots
* ❓ Interview Questions
* ⚠️ Troubleshooting
* 🌍 Real-World Examples
* 🛠️ Important Commands
* ✅ Practical Tasks

The goal is to understand **why something is used**, **how it works**, and **how to perform it practically**.

---

# 🧩 Modules Completed

## Module 1 - Introduction to Jenkins

Topics covered:

* What is Jenkins?
* Why Jenkins is used
* Jenkins in DevOps
* CI/CD overview
* Jenkins use cases
* Basic Jenkins architecture
* Jenkins terminology

---

## Module 2 - CI/CD Fundamentals

Topics covered:

* Continuous Integration
* Continuous Delivery
* Continuous Deployment
* CI/CD workflow
* Benefits of CI/CD
* Jenkins role in CI/CD
* Real-world CI/CD examples

---

## Module 3 - Jenkins Installation

Hands-on topics covered:

* Installing Java
* Installing Jenkins
* Running Jenkins on Ubuntu
* Running Jenkins on AWS EC2
* Jenkins service management
* Unlocking Jenkins
* Creating the first administrator account
* Initial Jenkins configuration

Example commands practiced:

```bash
java -version
sudo systemctl status jenkins
sudo systemctl start jenkins
sudo systemctl stop jenkins
sudo systemctl restart jenkins
```

---

## Module 4 - Jenkins Dashboard

Topics covered:

* Jenkins Dashboard
* Manage Jenkins
* New Item
* Build Queue
* Build Executor
* Job management
* Jenkins administration basics
* Navigating the Jenkins UI

---

## Module 5 - Jenkins Freestyle Jobs

This module focuses on understanding Jenkins Jobs and creating our first **Freestyle Project**.

Topics covered:

* What is a Jenkins Job?
* Types of Jenkins Jobs
* What is a Freestyle Project?
* Freestyle vs Pipeline
* Creating a Jenkins Freestyle Job
* Build Now
* Execute Shell
* Jenkins Workspace
* Build History
* Build Numbers
* Build Status
* Console Output
* Job Configuration
* Build Triggers
* Build Environment
* Post-build Actions
* Rename Jobs
* Disable Jobs
* Enable Jobs
* Delete Jobs
* Real-world CI workflow

Linux commands practiced through Jenkins:

```bash
pwd
whoami
hostname
date
ls
```

Practical work completed:

* Created a Freestyle Job
* Executed Linux commands
* Used Execute Shell
* Practiced successful builds
* Practiced failed builds
* Viewed Console Output
* Understood Build History
* Renamed Jobs
* Disabled and enabled Jobs
* Deleted temporary Jobs

---

## Module 6 - Jenkins + GitHub Integration

This module focuses on connecting Jenkins with GitHub and understanding the basic CI workflow.

Topics covered:

* GitHub overview
* Why Jenkins integrates with GitHub
* Continuous Integration
* Installing Git
* Verifying Git installation
* Configuring Git in Jenkins
* GitHub Personal Access Token
* Jenkins Credentials
* Source Code Management
* Connecting Jenkins to GitHub
* Cloning GitHub repositories
* Jenkins Workspace
* Building code from GitHub
* Poll SCM
* GitHub Webhooks
* Real-world CI workflow

Git commands practiced:

```bash
git --version
which git
```

Git installation:

```bash
sudo apt update
sudo apt install git -y
```

Example Git installation verification:

```text
git version 2.53.0
/usr/bin/git
```

Practical work completed:

* Verified Git installation
* Configured Git in Jenkins
* Created a GitHub Personal Access Token
* Added Jenkins Credentials
* Connected Jenkins to GitHub
* Configured Source Code Management
* Configured repository URL
* Configured the branch
* Successfully cloned a GitHub repository
* Built a project from GitHub
* Used Jenkins Workspace
* Practiced Execute Shell
* Learned Poll SCM
* Learned GitHub Webhooks
* Understood the real-world CI workflow

### Basic CI Workflow

```text
Developer
    ↓
GitHub
    ↓
Jenkins
    ↓
Git Clone
    ↓
Workspace
    ↓
Build
    ↓
Test
    ↓
Deploy
```

---

# 🔐 Jenkins Credentials & Security

While working with GitHub integration, I also learned the importance of securely managing credentials.

Instead of placing tokens directly inside scripts or Jenkins jobs, Jenkins Credentials can be used to securely store authentication information.

Important security practices:

* Never commit Personal Access Tokens to GitHub
* Never expose credentials in Jenkinsfiles
* Never publish credentials in screenshots
* Never hard-code secrets inside shell scripts
* Use Jenkins Credentials for authentication

---

# ⚠️ Troubleshooting Experience

During this learning journey, I have practiced troubleshooting issues related to:

* Jenkins installation
* Java installation
* Jenkins service management
* Port 8080 accessibility
* AWS EC2 Security Groups
* Git installation
* Git configuration
* GitHub authentication
* Jenkins credentials
* Git repository access
* Build failures
* Console Output errors
* Workspace issues

I document these problems and their solutions so that I can improve my troubleshooting skills.

---

# 🎯 Skills Gained So Far

Through the completed modules, I have developed hands-on knowledge of:

* Jenkins Fundamentals
* Jenkins Dashboard
* Jenkins Jobs
* Freestyle Projects
* Jenkins Workspace
* Build History
* Console Output
* Jenkins Configuration
* Build Triggers
* Git
* GitHub
* GitHub Integration
* Source Code Management
* Jenkins Credentials
* Personal Access Tokens
* Poll SCM
* GitHub Webhooks
* Continuous Integration
* Continuous Delivery
* Continuous Deployment
* Linux Administration
* AWS EC2
* Java / OpenJDK
* System Services
* Shell Commands
* Basic CI/CD Workflows

---

# 🔄 Jenkins + GitHub Workflow

The basic workflow I have practiced so far is:

```text
       Developer
           │
           ▼
       GitHub
           │
           ▼
        Jenkins
           │
           ▼
       Git Clone
           │
           ▼
        Workspace
           │
           ▼
         Build
           │
           ▼
          Test
           │
           ▼
        Deploy
```

This workflow represents the foundation of a modern CI/CD pipeline.

---

# 🚀 Upcoming Topics

After completing the basic Jenkins and GitHub integration concepts, the next stage of this learning journey will focus on more advanced Jenkins concepts.

Planned topics include:

* Jenkins Pipelines
* Jenkinsfile
* Pipeline as Code
* Declarative Pipeline
* Scripted Pipeline
* Pipeline Stages
* Environment Variables
* Parameters
* Build Triggers
* GitHub Webhooks
* Docker Integration
* Jenkins Agents
* Controller-Agent Architecture
* Maven Integration
* SonarQube Integration
* Nexus Integration
* Kubernetes Integration
* Credentials Management
* Shared Libraries
* Real-World CI/CD Project

---

# 🏗️ Future CI/CD Project

The final goal of this repository is to build a practical CI/CD project demonstrating a workflow similar to:

```text
Developer
    │
    ▼
  GitHub
    │
    ▼
  Jenkins
    │
    ├── Clone Source Code
    │
    ├── Build
    │
    ├── Test
    │
    ├── Code Quality
    │
    ├── Security Checks
    │
    ├── Docker Build
    │
    └── Deployment
```

The project will be expanded as I learn more DevOps tools and Jenkins integrations.

---

# 📈 Learning Philosophy

I believe the best way to learn DevOps is by:

* Understanding concepts clearly
* Practicing every concept hands-on
* Running commands myself
* Troubleshooting real problems
* Building projects
* Documenting the learning process
* Preparing for interviews
* Continuously improving

This repository is not intended to be just a collection of notes.

It represents my **practical Jenkins learning journey**.

---

# 📌 Current Progress

```text
Jenkins Fundamentals        ✅
CI/CD Fundamentals          ✅
Jenkins Installation       ✅
Jenkins Dashboard          ✅
Freestyle Jobs             ✅
GitHub Integration         ✅
Jenkins Pipelines          🔄
Docker Integration         ⏳
Jenkins Agents             ⏳
Real-World CI/CD Project   ⏳
```

---

# ⭐ Final Goal

The ultimate goal of this repository is to progress from:

```text
Jenkins Beginner
      ↓
Jenkins User
      ↓
Jenkins Administrator
      ↓
CI/CD Practitioner
      ↓
DevOps Engineer
```

I will continue updating this repository as I learn new Jenkins concepts, complete hands-on labs, solve troubleshooting problems, and build real-world CI/CD projects.

---

# 🤝 Feedback & Contributions

This is primarily a personal learning repository, but feedback, suggestions, and corrections are always welcome.

If you find something that can be improved, feel free to open an issue or suggest an improvement.

---

# ⭐ Support My Learning Journey

If you find this repository useful, feel free to **⭐ Star the repository** and follow my DevOps learning journey.

Thank you for visiting my **Jenkins Zero to Hero** repository! 🚀

**Learning → Practicing → Troubleshooting → Documenting → Building**


#module 9 jenkins webhook

