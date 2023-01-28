pipeline {
    agent none
    stages {
        stage('Build') {
            agent { 
                label 'slave1'
            }
            steps {
                script {
                        if(1 == 1){
                        echo "read config file is 1"    
                        }
                        else
                        {
                        echo "read config file is not 1"
                    }
                }
            }
        }
        stage('Test on slave1') {
            agent { 
                label 'slave1'
            }
            steps {
                script {
                    if (2 == 2)
                    {
                    echo "Download Artifacts is 2"
                    }
                    else if (3 == 3)
                    {
                    echo "Download Artifacts is 3"
                    }
                }
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
                script {
                    if (2 == 2)
                    {
                    echo "Download Artifacts is 2"
                    }
                    else if (3 == 3)
                    {
                    echo "Download Artifacts is 3"
                    }
                }
            }
            post {
                always {
                    echo "build 5555555"
                }
            }
        }
    }
}