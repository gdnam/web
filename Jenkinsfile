pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git credentialsId: '5596cd6c-b80c-44f4-899b-bc98f7a951b5', url: 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    stage('build code')
    {
        steps
        {
            bat script: 'mvn complie'
        }
    }
    stage('Run test ')
    {
        steps 
        {
            bat script: 'mvn test -Dbrower=localchrome'
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