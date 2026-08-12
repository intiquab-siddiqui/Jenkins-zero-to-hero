# Module 7 - Jenkins Pipeline

## Topics Covered

### Lesson 1 - What is Jenkins Pipeline?
- Jenkins Pipeline
- Pipeline Automation
- Pipeline as Code

### Lesson 2 - Freestyle Project vs Pipeline
- Freestyle Project
- Jenkins Pipeline
- Advantages of Pipeline

### Lesson 3 - What is a Jenkinsfile?
- Jenkinsfile
- Pipeline as Code
- Jenkinsfile in GitHub

### Lesson 4 - Declarative Pipeline Structure
- pipeline
- agent
- stages
- stage
- steps

### Lesson 5 - Stages & Steps
- Stages
- Steps
- echo
- sh
- Linux Commands in Pipeline

### Lesson 6 - Create First Pipeline
- Create Pipeline Job
- Declarative Pipeline
- Build and Test Stages
- Console Output

### Lesson 7 - Pipeline from GitHub
- Pipeline script from SCM
- GitHub Repository
- Jenkinsfile
- GitHub Credentials

### Lesson 8 - Real-World CI Pipeline
- Checkout
- Build
- Test
- CI Workflow

### Lesson 9 - Interview Preparation
- Jenkins Pipeline Interview Questions
- Jenkinsfile Interview Questions
- Pipeline as Code

---

## Practical Work Completed

- Created first Jenkins Pipeline
- Used Declarative Pipeline syntax
- Used `agent any`
- Created multiple stages
- Executed Linux commands using `sh`
- Stored Jenkinsfile in GitHub
- Configured Pipeline from SCM
- Connected Jenkins Pipeline with GitHub
- Created Checkout, Build and Test stages
- Successfully executed the pipeline

---

## Pipeline Structure

```text
pipeline
   |
   ├── agent
   |
   └── stages
        |
        ├── Checkout
        |
        ├── Build
        |
        └── Test





pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'pwd'
                sh 'whoami'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'date'
                sh 'hostname'
            }
        }

    }
}




##Key Learnings

Pipeline

An automated workflow used to build, test and deploy applications.

Jenkinsfile

A file used to define a Jenkins Pipeline as code.

Stage

Represents a major phase of the pipeline.

Steps

Contains the actual commands or actions executed by Jenkins.

Agent

Defines where the pipeline should run.

Pipeline as Code

Defining the CI/CD workflow in code and storing it in version control.

Final Workflow

Developer
    |
    v
GitHub
    |
    v
Jenkins
    |
    v
Jenkinsfile
    |
    v
Checkout
    |
    v
Build
    |
    v
Test
    |
    v
SUCCESS

Status

✅ Module 7 Completed
