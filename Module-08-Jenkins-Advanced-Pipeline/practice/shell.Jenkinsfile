pipeline {
    agent any

    stages {
        stage('Linux Commands') {
            steps {
                sh '''
                    echo "Starting Linux commands"
                    pwd
                    whoami
                    hostname
                    date
                    ls -la
                '''
            }
        }
    }
}
