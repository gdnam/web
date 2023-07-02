pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git credentialsId: '78e5cc69-355e-4570-9048-8bf7e600013c', url: 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    stage('build code')
    {
        steps
        {
            script: 'mvn complie'
        }
    }
    stage('Run test ')
    {
        steps 
        {
            script: 'mvn test -Dbrower=localchrome'
        }
    }
    stage('Publish HTML Reports')
    {
        steps
        {
         publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: '', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
        }
    }
    }
}