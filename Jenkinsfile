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
        build 'BuidAppJob'
    }
    stage(' Results ')
    {
        build 'TestAppJob'
    }
    }
}



