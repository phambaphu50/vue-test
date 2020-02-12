pipeline {
    agent {
        docker {
            image 'node:12-alpine' 
            args '-p 8080:8080' 
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Deploy') { 
            steps {
                sh './deliver.sh' 
            }
        }
    }
}
