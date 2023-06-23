pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git credentialsId: '8a961f26-94e1-4784-a842-e207eb947187', url: 'https://github.com/gdnam/web.git'
                echo 'Hello World'
            }
        }
    stage('build code')
    {
        build 'BuidAppJob'
    }
    stage(' Results ')
    {
        build 'TestAppJob'
    }
    }
}



