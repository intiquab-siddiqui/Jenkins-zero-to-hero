pipeline {
    
    agent any 
    
    stages {
        stage('Build') {
            steps {
                echo 'building application'
            }
        }
        stage('test') {
            steps {
                echo 'running tests'
            }
        }
    }
    post {
        success {
            echo 'pipeline completed successfully!'
        }
        
        failure {
            echo 'pipeline failed'
        }
        
        always {
            echo 'pipeline excution completed'
        }
            
    }
}
