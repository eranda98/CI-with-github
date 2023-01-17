pipeline {
    agent any

    stages {
        stage('build from github') {
            steps {
                echo 'fetch code'
                git branch: 'main', url: 'https://github.com/eranda98/CI-with-github.git'
                echo 'build code'
            }
        }
        stage('test from github') {
            steps {
                echo 'running test1'
                echo 'running test2'
            }
        }
    }
}
