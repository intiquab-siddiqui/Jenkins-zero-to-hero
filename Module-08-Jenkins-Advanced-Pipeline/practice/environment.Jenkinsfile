pipeline {
    agent any
    
    environment {
        APP_NAME = 'jenkins demo'
        ENVIRONMENT = 'development'
    
    }
    stages {

        stage('Build') {
            steps {
                echo "Application: ${APP_NAME}"
                echo "Environment: ${ENVIRONMENT}"
            }
        }

        stage('Test') {
            steps {
                echo "Testing ${APP_NAME}"
                sh 'echo "Running on $(hostname)"'
            }
        }

    }
}
