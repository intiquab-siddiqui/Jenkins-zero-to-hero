# Module 4 - Jenkins Dashboard

## 📚 Topics Covered

### Lesson 1 - Jenkins Dashboard Overview
- What is Jenkins Dashboard?
- Dashboard Layout
- Left Sidebar
- Main Workspace
- Top Navigation

### Lesson 2 - Home Page Components
- New Item
- People
- Build History
- Manage Jenkins
- My Views

### Lesson 3 - Manage Jenkins
- Administration Center
- Plugins
- Credentials
- Global Tool Configuration
- Nodes (Agents)
- Security
- System Information

### Lesson 4 - Dashboard Sidebar
- New Item
- People
- Build History
- Manage Jenkins
- My Views

### Lesson 5 - Build History
- Build Number
- Build Status
- Success
- Failure
- Unstable
- Aborted
- Console Output

### Lesson 6 - Users & Security
- Users
- Authentication
- Authorization
- Security Basics

### Lesson 7 - Dashboard Navigation
- Jenkins Logo
- Search
- Breadcrumb Navigation
- Navigation Flow

---

# 💼 Interview Questions & Answers

## 1. What is Jenkins Dashboard?

**Answer:**
Jenkins Dashboard is the main user interface of Jenkins where users create, monitor, and manage jobs, pipelines, builds, users, nodes, and system settings.

---

## 2. What is Manage Jenkins?

**Answer:**
Manage Jenkins is the administration center used to configure Jenkins. It allows administrators to manage plugins, credentials, security, system settings, build agents, and tools.

---

## 3. Why do we use Plugins?

**Answer:**
Plugins extend Jenkins functionality by integrating it with external tools and services.

**Examples:**
- Git
- Docker
- Maven
- SonarQube
- Kubernetes
- Slack
- AWS

---

## 4. Why do we use Credentials?

**Answer:**
Credentials securely store sensitive information such as usernames, passwords, SSH keys, and API tokens. This prevents secrets from being exposed in Jenkins jobs and pipelines.

---

## 5. What is Global Tool Configuration?

**Answer:**
Global Tool Configuration is used to configure development tools that Jenkins uses during builds.

**Examples:**
- Git
- JDK
- Maven
- Gradle
- Docker

---

## 6. What is Build History?

**Answer:**
Build History displays all previous builds of a job, including their build numbers, timestamps, and build status.

It helps users:
- Track previous builds
- Identify failures
- Monitor successful builds
- Access build logs

---

## 7. What is Console Output?

**Answer:**
Console Output is the detailed log generated during a Jenkins build.

It helps to:
- Monitor build progress
- Identify errors
- Debug failed builds
- Verify executed commands

---

## 8. What is Authentication?

**Answer:**
Authentication is the process of verifying a user's identity before granting access to Jenkins.

Examples:
- Username & Password
- LDAP
- Active Directory
- GitHub Login
- Google OAuth

---

## 9. What is Authorization?

**Answer:**
Authorization determines what an authenticated user is allowed to do inside Jenkins.

Examples:
- View Jobs
- Create Jobs
- Delete Jobs
- Configure Pipelines
- Manage Jenkins

---

## 10. Difference between Authentication and Authorization

| Authentication | Authorization |
|----------------|---------------|
| Verifies who the user is. | Determines what the user is allowed to do. |
| Happens first. | Happens after authentication. |
| Uses login credentials. | Uses roles and permissions. |
| Example: Login with username and password. | Example: Admin can create jobs, Viewer can only view jobs. |

---

# 📝 Key Takeaways

- Jenkins Dashboard is the central place for managing Jenkins.
- Manage Jenkins contains all administrative settings.
- Plugins extend Jenkins functionality.
- Credentials securely store sensitive information.
- Build History helps monitor previous builds.
- Console Output is used for troubleshooting.
- Authentication verifies identity.
- Authorization controls user permissions.

---

# 📂 Repository Structure

```
Module-04-Jenkins-Dashboard/
│
├── README.md
├── handwritten-notes/
├── screenshots/
└── interview-questions.md
```

---

# 📌 Status

✅ Module 4 Completed

---

## 🙌 Author

**Intiquab Siddiqui**

Learning DevOps step by step with hands-on practice and interview preparation.
