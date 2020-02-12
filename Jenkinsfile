pipeline {
    agent {
        docker {
            image 'node:12-alpine' 
            args '-p 3000:8080' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
