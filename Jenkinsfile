pipeline {
    agent any

    stages {
        stage('clone from github'){
            steps{
                dir("CI_with_github"){
                    echo 'clone git repo'
                    git branch: 'main', changelog: false, poll: false, url: 'https://github.com/eranda98/CI-with-github.git'
                    bat 'dir'
                }
            }
        }
        stage('build from github') {
            steps {
                dir("CI_with_github"){
                    echo 'pip install -r requirements.txt'
                    bat 'C:/Program Files/Python311/Scripts/pip install -r requirements.txt'
                    bat 'C:/Program Files/Python311/python app.py'
                }
            }
        }
        stage('test from github') {
            steps {
                echo 'running test1'
                echo 'running test2'
            }
        }
        stage('deploying from github'){
            steps{
                echo "deployement"
            }
        }
    }
}
