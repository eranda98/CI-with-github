pipeline {
    agent any
    
    environment {
        def pip = "C:/Users/erand/AppData/Local/Programs/Python/Python311/Scripts/pip"
        def python = "C:/Users/erand/AppData/Local/Programs/Python/Python311/python"
    }

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
                dir("CI_Jenkins"){
                    echo 'pip install -r requirements.txt'
                    bat "${pip} install -r requirements.txt"
                }
            }
        }
        stage('test from github') {
            steps {
                dir("CI_Jenkins"){
                    echo "pyhton -m unittest"
                    bat "${python} -m unittest"
                }
            }
        }
        stage('deploying from github'){
            steps{
                echo "deployement"
            }
        }
    }
}
