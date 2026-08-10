# Module 5 - Jenkins Freestyle Jobs

## 📚 Topics Covered

### Lesson 1 - Jenkins Job

#### What is a Jenkins Job?
A Jenkins Job is a task or automation that Jenkins performs. It can build code, run tests, execute shell scripts, deploy applications, or perform any automated task.

#### Why Jenkins Jobs are used?
Jenkins Jobs help automate repetitive tasks such as:
- Building applications
- Running automated tests
- Deploying applications
- Executing shell scripts
- Scheduling tasks

#### Types of Jenkins Jobs
- Freestyle Project
- Pipeline
- Multi-configuration Project
- Folder
- Multibranch Pipeline
- Organization Folder

---

### Lesson 2 - Freestyle Project

#### What is a Freestyle Project?
A Freestyle Project is the simplest and most beginner-friendly Jenkins job type. It allows users to execute shell commands, build software, and automate tasks without writing a pipeline script.

#### Freestyle vs Pipeline

| Freestyle | Pipeline |
|------------|-----------|
| GUI-based configuration | Code-based configuration |
| Easy for beginners | Better for complex CI/CD |
| Limited flexibility | Highly flexible |
| Harder to version control | Stored in Git using Jenkinsfile |

#### Execute Shell
The **Execute Shell** build step allows Jenkins to run Linux shell commands during the build.

Example:

```bash
echo "Hello Jenkins"
pwd
whoami
date
```

---

### Lesson 3 - Create First Job

Steps:

1. Click **New Item**
2. Enter Job Name
3. Select **Freestyle Project**
4. Click **OK**
5. Configure the job
6. Add Build Step → Execute Shell
7. Save the job

---

### Lesson 4 - Build Now

#### Manual Build
Click **Build Now** to execute the job manually.

#### Execute Shell
Runs Linux commands.

Example:

```bash
echo "Build Started"
hostname
pwd
date
```

#### Linux Commands Practiced

```bash
pwd
whoami
hostname
date
ls
```

#### Workspace
Workspace is the directory where Jenkins stores project files during execution.

Default:

```
/var/lib/jenkins/workspace/
```

---

### Lesson 5 - Build History

#### Build Numbers
Each build receives a unique number.

Example:

```
#1
#2
#3
```

#### Build Status

✅ SUCCESS
- Build completed successfully.

❌ FAILURE
- Build failed due to errors.

🛑 ABORTED
- Build was manually stopped.

⚠️ UNSTABLE
- Build completed but some tests failed.

---

### Lesson 6 - Console Output

#### Build Logs
Console Output displays everything Jenkins executes.

It includes:
- Linux commands
- Errors
- Warnings
- Build progress
- Output of scripts

#### Troubleshooting

Console Output helps identify:

- Syntax errors
- Missing files
- Permission issues
- Build failures

#### Workspace
Shows where files are stored during execution.

#### Errors
Examples:

```
command not found

permission denied

No such file or directory
```

---

### Lesson 7 - Configure

Main Configuration Sections

### General
Basic job settings.

### Source Code Management (SCM)
Connect Jenkins with Git repositories.

### Build Triggers
Automatically start builds.

Examples:
- Poll SCM
- Build periodically
- GitHub Webhook

### Build Environment
Prepare environment before build.

Examples:
- Delete workspace
- Secret files
- Environment variables

### Build Steps
Actual tasks Jenkins performs.

Examples:
- Execute Shell
- Invoke Gradle
- Maven Build

### Post-build Actions
Runs after build completion.

Examples:
- Archive Artifacts
- Email Notifications
- Publish Reports

---

### Lesson 8 - Rename, Disable & Delete

#### Rename Job
Change the job name.

#### Disable Job
Temporarily prevent builds from running.

#### Enable Job
Re-enable the disabled job.

#### Delete Job
Permanently remove the job from Jenkins.

---

### Lesson 9 - Real World CI Workflow

```
Developer
      │
      ▼
 GitHub Repository
      │
      ▼
 Jenkins Job
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

# Practical Completed

- Created first Freestyle Job
- Executed Linux commands
- Used Execute Shell
- Practiced successful build
- Practiced failed build
- Viewed Console Output
- Learned Build History
- Renamed Job
- Disabled Job
- Enabled Job
- Deleted temporary Job

---

# Interview Questions

### 1. What is a Jenkins Job?

A Jenkins Job is an automation task that Jenkins performs such as building, testing, or deploying an application.

---

### 2. What is a Freestyle Project?

A Freestyle Project is the simplest Jenkins job type used to automate tasks through the Jenkins UI.

---

### 3. What is Execute Shell?

Execute Shell is a build step that allows Jenkins to run Linux shell commands.

---

### 4. What does Build Now do?

It manually starts a Jenkins build.

---

### 5. What is Build History?

Build History displays all previous builds with their status and build numbers.

---

### 6. What is Console Output?

Console Output shows detailed logs of the build process.

---

### 7. What is Workspace?

Workspace is the directory where Jenkins stores project files during execution.

---

### 8. Difference between SUCCESS and FAILURE?

SUCCESS means the build completed successfully.

FAILURE means the build stopped because of an error.

---

### 9. Difference between Freestyle and Pipeline?

Freestyle is GUI-based.

Pipeline is code-based using a Jenkinsfile.

---

### 10. Why do we disable a Jenkins Job?

To temporarily stop builds without deleting the job.

---

### 11. Can a disabled job be built?

No. It must be enabled before it can run again.

---

### 12. What is SCM?

SCM (Source Code Management) connects Jenkins to version control systems like Git.

---

### 13. What are Build Triggers?

They automatically start builds based on events or schedules.

---

### 14. What are Post-build Actions?

Tasks executed after the build, such as sending emails or archiving artifacts.

---

### 15. Where does Jenkins store job files?

Inside the Jenkins Home directory.

Example:

```
/var/lib/jenkins/jobs/
```

---

# Module Summary

✅ Learned Jenkins Jobs

✅ Created Freestyle Project

✅ Executed Linux Commands

✅ Understood Workspace

✅ Learned Build History

✅ Viewed Console Output

✅ Configured Jenkins Jobs

✅ Renamed Jobs

✅ Disabled & Enabled Jobs

✅ Deleted Jobs

✅ Understood Real CI Workflow

---

# Status

✅ Module 5 Completed Successfully
