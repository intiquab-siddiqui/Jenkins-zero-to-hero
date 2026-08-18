pipeline {

    agent any

    stages {

        stage('Use Credential') {
            steps {
                withCredentials([
                    string(
                        credentialsId: 'demo-secret',
                        variable: 'MY_SECRET'
                    )
                ]) {
                    sh 'echo "Credential is available to the pipeline"'
                }
            }
        }

    }
}
