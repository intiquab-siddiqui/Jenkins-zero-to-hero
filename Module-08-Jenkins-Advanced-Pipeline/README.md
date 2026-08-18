# Module 8 – Jenkins Advanced Pipeline

## Overview

In this module, I learned advanced Jenkins Pipeline concepts and integrated Jenkins with Docker to create and run Docker containers.

## Topics Covered

### 1. Environment Variables

Environment variables store configuration values that can be reused throughout a Jenkins Pipeline.

Example:

```groovy
environment {
    APP_NAME = 'jenkins-demo'
    ENVIRONMENT = 'development'
}


2. Jenkins Parameters

Parameters allow users to provide input when triggering a build.

Example:

parameters {
    choice(
        name: 'ENVIRONMENT',
        choices: ['development', 'testing', 'production'],
        description: 'Select the deployment environment'
    )
}

The selected value can be accessed using:

params.ENVIRONMENT
3. Post Actions

The post section allows Jenkins to perform actions after pipeline execution.

Common conditions:

success
failure
always
unstable
aborted
4. When Conditions

The when directive conditionally executes a stage.

Example:

when {
    expression {
        params.ENVIRONMENT == 'production'
    }
}
5. Jenkins Credentials

Sensitive information such as passwords, tokens, and SSH keys should not be hard-coded inside Jenkinsfiles.

Jenkins Credentials securely stores these values.

withCredentials can be used to access credentials inside a pipeline.

6. Multiple Shell Commands

Multiple Linux commands can be executed using a multi-line sh block.

sh '''
    pwd
    whoami
    hostname
    date
'''
7. Build Failure Handling

Jenkins normally fails a pipeline when a shell command returns a non-zero exit code.

Using:

returnStatus: true

allows the pipeline to capture the exit status and handle the result manually.

8. Jenkins and Docker

I configured Jenkins to communicate with Docker by adding the Jenkins user to the Docker group.

The setup was verified using:

sudo -u jenkins docker --version
9. Docker Image Build

Jenkins was used to build a Docker image:

docker build -t jenkins-docker-demo:v1 .
10. Docker Container

Jenkins was also used to run a Docker container:

docker run -d --name jenkins-docker-container -p 8081:80 jenkins-docker-demo:v1

The Nginx application was successfully accessed through the browser.

Final CI Pipeline

The final pipeline combined:

Parameters
    ↓
Build
    ↓
Test
    ↓
Docker Build
    ↓
Docker Run
    ↓
Verify Container
    ↓
Post Actions

Troubleshooting

Docker Permission Error

Jenkins initially received a Docker permission error.

Solution:

sudo usermod -aG docker jenkins
sudo systemctl restart jenkins

Then Docker access was verified.

Dockerfile Not Found

Jenkins initially could not find the Dockerfile because it was not present in the Jenkins workspace.

The Dockerfile was placed in the correct workspace and the pipeline successfully built the image.

Docker Container Name Conflict

A container-name conflict was handled using:

docker rm -f jenkins-docker-final-container || true

This allows the pipeline to remove an existing container before creating a new one.

Practical Outcome

By the end of this module, I successfully created a Jenkins Pipeline that:

Accepts environment parameters
Builds and tests the application
Builds a Docker image
Runs a Docker container
Verifies the running container
Handles success and failure using post actions
Deploys an Nginx container accessible through the browser
Skills Practiced
Jenkins Declarative Pipeline
Environment Variables
Parameters
Conditional Stages
Post Actions
Jenkins Credentials
Shell Scripting
Error Handling
Docker Integration
Docker Image Building
Docker Container Management
CI/CD Troubleshooting


