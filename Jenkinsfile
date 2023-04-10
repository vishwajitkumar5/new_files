@Library('my-shared-library') _

pipeline {
    agent any
    environment {
        //PATH="/opt/apache-maven-3.6.3/bin:$PATH"
        PATH="C:\Program Files\apache-maven-3.6.3:$PATH\bin"
    }
    
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
