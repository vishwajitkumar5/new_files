@Library('my-shared-library') _

pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/vishwajitkumar5/new_files.git']]])
            }
        }

        stage('Unit Test maven') {
            
            steps {
                script{
                    
                    mvnTest()
                }
            }
        }
    }
}
