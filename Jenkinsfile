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
