pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    stage('build code')
    {
        steps
        {
            echo 'Buid App'
        }
    }
    stage('Run test ')
    {
        steps 
        {
            echo 'Test App'
        }
    }
    stage('Publish HTML Reports')
    {
        steps
        {
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: '', reportFiles: 'index.html', reportName: 'Pipeline', reportTitles: '', useWrapperFileDirectly: true])
        }
    }
    }
}