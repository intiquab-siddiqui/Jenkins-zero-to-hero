# Module 6 - Jenkins + GitHub Integration

## 📚 Topics Covered

### Lesson 1 - Why Integrate Jenkins with GitHub?

#### GitHub Overview

GitHub is a platform used to store, manage, and collaborate on source code using Git.

Developers push their code to GitHub, and Jenkins can automatically retrieve that code and perform CI/CD tasks.

#### Continuous Integration (CI)

Continuous Integration is the practice of automatically building and testing code whenever developers make changes.

#### Benefits of Jenkins + GitHub Integration

* Automates builds when code changes
* Provides faster feedback to developers
* Reduces manual work
* Improves collaboration
* Provides reliable and consistent builds

---

### Lesson 2 - Install Git & Verify Git

Jenkins needs Git to communicate with GitHub repositories.

#### Install Git on Ubuntu

```bash
sudo apt update
sudo apt install git -y
```

#### Verify Git Installation

```bash
git --version
```

Example:

```text
git version 2.53.0
```

#### Check Git Location

```bash
which git
```

Example:

```text
/usr/bin/git
```

---

### Lesson 3 - Configure Git in Jenkins

Jenkins needs to know where Git is installed.

Steps:

1. Go to **Manage Jenkins**
2. Open **Tools / Global Tool Configuration**
3. Find **Git installations**
4. Add Git installation
5. Give it a name

Example:

```text
Name: Default
Path: /usr/bin/git
```

6. Save the configuration.

---

### Lesson 4 - GitHub Personal Access Token (PAT)

A Personal Access Token (PAT) can be used to authenticate Jenkins with GitHub when password authentication is not appropriate.

#### Create a GitHub PAT

General steps:

1. Open GitHub
2. Go to Settings
3. Open Developer Settings
4. Open Personal Access Tokens
5. Create a new token
6. Give the token an appropriate name
7. Set an expiration date
8. Select only the permissions required
9. Generate the token
10. Copy and securely store the token

⚠️ **Important:** Never publish a PAT in GitHub, Jenkinsfiles, screenshots, or public repositories.

#### Token Permissions

Give the token only the permissions required for the task.

For example, repository access may be required when Jenkins needs to access a private repository.

---

### Lesson 5 - Jenkins Credentials

Jenkins Credentials allow us to securely store authentication information.

Instead of writing a GitHub token directly inside a job configuration or script, Jenkins stores it securely.

#### Store GitHub PAT

Steps:

1. Go to **Manage Jenkins**
2. Open **Credentials**
3. Select the appropriate credentials store
4. Click **Add Credentials**
5. Select:

```text
Kind: Username with password
```

6. Enter GitHub username
7. Enter the PAT as the password
8. Add an ID

Example:

```text
ID: github-pat
Description: GitHub PAT
```

9. Save.

### Important

Never expose credentials in:

* Console Output
* GitHub repositories
* Jenkinsfiles
* Screenshots
* Shell scripts

---

### Lesson 6 - Connect Jenkins to GitHub

Now Jenkins can be connected to a GitHub repository.

Steps:

1. Create/Open a Jenkins Freestyle Project
2. Click **Configure**
3. Find **Source Code Management**
4. Select **Git**
5. Enter the GitHub Repository URL
6. Select Jenkins Credentials
7. Configure the branch
8. Save

Example Repository URL:

```text
https://github.com/username/repository.git
```

Example Branch:

```text
*/main
```

Jenkins will use Git to clone the repository.

---

### Lesson 7 - Build Code from GitHub

When a Jenkins job runs, Jenkins can clone the source code from GitHub into its workspace.

#### Git Clone

Jenkins performs the equivalent of getting the repository source code using Git.

The code is then available inside the Jenkins workspace.

#### Jenkins Workspace

Example:

```text
/var/lib/jenkins/workspace/<job-name>/
```

The workspace contains the files downloaded from GitHub.

#### Execute Shell

After Jenkins downloads the code, we can execute commands against the project.

Example:

```bash
echo "Building project from GitHub"

pwd

ls -la

echo "Build Successful"
```

---

### Lesson 8 - Poll SCM vs Webhooks

Jenkins provides different ways to automatically trigger builds.

## Poll SCM

Jenkins periodically checks the GitHub repository for changes.

Example cron schedule:

```text
H/5 * * * *
```

This means Jenkins checks approximately every 5 minutes.

### Advantages

* Easy to understand
* Simple to configure

### Disadvantage

Jenkins checks periodically instead of receiving an immediate notification.

---

## GitHub Webhooks

A webhook allows GitHub to notify Jenkins when an event such as a push occurs.

### Workflow

```text
Developer
    ↓
Push Code
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Build
```

### Advantages

* Near real-time triggering
* Faster than polling
* Efficient for CI/CD

---

### Lesson 9 - Real World CI Workflow

```text
Developer
     ↓
GitHub
     ↓
Jenkins
     ↓
Clone
     ↓
Build
     ↓
Test
     ↓
Deploy
```

### Real-World Example

1. Developer writes code
2. Developer pushes code to GitHub
3. GitHub notifies Jenkins or Jenkins detects the change
4. Jenkins clones the repository
5. Jenkins builds the application
6. Jenkins runs tests
7. Jenkins deploys the application

This is the basic foundation of a CI/CD workflow.

---

# 🔄 CI Workflow

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
   Clone
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

---

# 🛠️ Practical Completed

* ✅ Verified Git installation
* ✅ Used `git --version`
* ✅ Used `which git`
* ✅ Configured Git in Jenkins
* ✅ Verified Git installation path
* ✅ Created GitHub Personal Access Token
* ✅ Added Jenkins Credentials
* ✅ Connected Jenkins to GitHub
* ✅ Configured Source Code Management
* ✅ Configured repository URL
* ✅ Configured branch
* ✅ Successfully cloned GitHub repository
* ✅ Built project from GitHub
* ✅ Used Jenkins Workspace
* ✅ Practiced Execute Shell
* ✅ Learned Poll SCM
* ✅ Learned GitHub Webhooks
* ✅ Understood real-world CI workflow

---

# 🎯 Interview Questions

### 1. Why do we integrate Jenkins with GitHub?

Jenkins integrates with GitHub so that it can automatically retrieve source code and perform build, test, and deployment tasks.

---

### 2. What is Git?

Git is a distributed version control system used to track changes in source code.

---

### 3. What is GitHub?

GitHub is a platform for hosting Git repositories and collaborating on source code.

---

### 4. What is Continuous Integration?

Continuous Integration is the practice of automatically building and testing code whenever changes are integrated into a shared repository.

---

### 5. Why does Jenkins need Git?

Jenkins uses Git to clone and retrieve source code from Git repositories such as GitHub.

---

### 6. What does `git --version` do?

It displays the installed Git version.

Example:

```bash
git --version
```

---

### 7. What does `which git` do?

It shows the location of the Git executable.

Example:

```text
/usr/bin/git
```

---

### 8. Why do we configure Git in Jenkins?

Jenkins needs the Git installation path so it knows which Git executable to use when interacting with repositories.

---

### 9. What is a Personal Access Token?

A Personal Access Token is a credential used to authenticate applications or users with GitHub.

---

### 10. Why should we use Jenkins Credentials?

Jenkins Credentials provide a secure way to store authentication information instead of exposing secrets directly in jobs or scripts.

---

### 11. What is SCM?

SCM stands for **Source Code Management**.

It allows Jenkins to retrieve source code from version control systems such as Git.

---

### 12. What is the Jenkins Workspace?

The workspace is the directory where Jenkins checks out source code and performs build-related operations.

Example:

```text
/var/lib/jenkins/workspace/<job-name>/
```

---

### 13. What is Poll SCM?

Poll SCM periodically checks the source-code repository for changes and triggers a build when changes are detected.

---

### 14. What is a GitHub Webhook?

A GitHub Webhook allows GitHub to send an HTTP notification to Jenkins when an event such as a push occurs.

---

### 15. Poll SCM vs Webhook?

| Poll SCM              | Webhook                  |
| --------------------- | ------------------------ |
| Jenkins checks GitHub | GitHub notifies Jenkins  |
| Uses a schedule       | Event-driven             |
| Can introduce delay   | Near real-time           |
| Simple to understand  | More efficient for CI/CD |

---

### 16. What happens when Jenkins builds from GitHub?

A typical flow is:

```text
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

### 17. Why should credentials not be written directly in scripts?

Because credentials can be exposed to other users, logs, Git repositories, or attackers.

Jenkins Credentials should be used instead.

---

# 🧠 Important Commands

```bash
git --version
which git
```

Install Git:

```bash
sudo apt update
sudo apt install git -y
```

Check workspace:

```bash
pwd
```

View project files:

```bash
ls -la
```

---

# 📌 Important Jenkins Concepts Learned

```text
Git
 ↓
GitHub
 ↓
PAT
 ↓
Jenkins Credentials
 ↓
SCM
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

# 🚀 Key Takeaway

Jenkins + GitHub integration is the foundation of CI/CD.

When a developer pushes code to GitHub, Jenkins can retrieve the latest code, build it, test it, and eventually deploy it automatically.

The basic idea is:

```text
Developer → GitHub → Jenkins → Build → Test → Deploy
```

---

# 📊 Module 6 Summary

✅ Git Installation

✅ Git Verification

✅ Git Configuration in Jenkins

✅ GitHub PAT

✅ Jenkins Credentials

✅ GitHub SCM

✅ Repository Cloning

✅ Jenkins Workspace

✅ Build from GitHub

✅ Poll SCM

✅ GitHub Webhooks

✅ Real-World CI Workflow

---

# 🏆 Status

# ✅ Module 6 Completed Successfully

**Next:** Module 7 – Jenkins Pipelines
