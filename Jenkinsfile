pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git credentialsId: 'cac9b266-d2c2-47cc-a737-eba77d250e31', url: 'https://github.com/gdnam/web.git'
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
         publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, keepAll: true, reportDir: '', reportFiles: 'target/surefile-reposts/Index*.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])   
        }
    }
    }
}

