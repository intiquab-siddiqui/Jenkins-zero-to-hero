pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Starting Build'
                sh 'pwd'
                sh 'whoami'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh 'date'
                sh 'hostname'
            }
        }

    }
}
