pipeline {
    agent any
    tools{
        maven 'MAVEN'
    }
    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q mavenjava"
                bat "git clone provide your github link"
                bat "mvn clean -f Jenkinsfile"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Jenkinsfile" #project name#
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Jenkinsfile"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Jenkinsfile"
            }
        }
    }
}
