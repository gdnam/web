pipeline {
    agent any

    stages {
        stage('Get Source Code') {
            steps {
                git credentialsId: '7943b714-42f1-45f1-8f0b-b2276b9d91f2', url: 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    }
}