pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/vishwajitkumar5/new_files.git']]])
            }
        }
    }
}