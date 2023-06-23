pipeline {
    agent any
    stages {
        stage('Build Code') {
            steps {
                 sh 'npm install'
            }
        }
        stage('Results') {
            steps {
               sh 'npm test'
            }
        }
    }
}