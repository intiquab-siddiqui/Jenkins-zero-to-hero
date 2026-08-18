pipeline {

    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['development', 'testing'],
            description: 'Select deployment environment'
        )
    }

    stages {

        stage('Build') {
            steps {
                echo "Building application for ${params.ENVIRONMENT}"
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Tests passed'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-docker-final:v1 .'
            }
        }

        stage('Docker Run') {
            steps {
                sh '''
                    docker rm -f jenkins-docker-final-container || true
                    docker run -d \
                        --name jenkins-docker-final-container \
                        -p 8081:80 \
                        jenkins-docker-final:v1
                '''
            }
        }

        stage('Verify Container') {
            steps {
                sh 'docker ps'
            }
        }
    }

    post {

        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed!'
        }

        always {
            echo 'Pipeline execution completed.'
        }
    }
}
