pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                echo "Build 11111"
            }
        }
        stage('Test on slave1') {
            agent { 
                label 'slave1'
            }
            steps {
                echo "Build 22222"
            }
            post {
                always {
                    echo "Build 333333"
                }
            }
        }
        stage('Test on slave2') {
            agent {
                label 'slave2'
            }
            steps {
                echo "build 444444"
            }
            post {
                always {
                    echo "build 5555555"
                }
            }
        }
    }
}