pipeline {
    agent any

    stages {
        stage('Get Source Code') {
            steps {
                git credentialsId: '8a961f26-94e1-4784-a842-e207eb947187', url: 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    stages('Build code')
    {
        steps
        {
            bat script: 'mvn complie'
        }
    }
    stages('run test')
    {
        steps{
            bat script: 'mvn test -Dbrower=localchrome'
        }
    }
    stages('Publish HTML Reports')
    {
        steps
        {
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: '', reportFiles: 'target/surefire-reports/index*.html', reportName: 'Pipeline', reportTitles: '', useWrapperFileDirectly: true])
        }
    }
    }
}
