pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['development', 'testing', 'production'],
            description: 'Select the deployment environment'
        )
    }

    stages {
        stage('Build') {
            steps {
                echo "Building application"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
