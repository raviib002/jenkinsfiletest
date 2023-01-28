pipeline {
    agent { label 'slave1' }
    stages {
        stage('Read Config File') {
            steps{
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
        stage('Download Artifacts') {
            steps{
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
        }       
        stage('Generate DB Scripts') {
            steps{
                script {
                    if (4 == 4)
                    {
                    echo "Generate DB Scripts is 4"
                    }
                }
            }
        }
        stage('Package') {
            steps{
                script {
                    echo "Package is 5"
                }
            }
            post{
                success {
                    script{
                        echo "Post success slave1"
                    }
                }
            }
        }
    }
}

pipeline {
    agent { label 'slave2' }
    stages {
        stage('Testing activity') {
            steps{
                script {
                    echo "Testing activity step slave2"
                }
            }
        }
        stage('Exctracting and excluding') {
            steps{
                script {
                    echo "Exctracting and excluding is not slave2"                    
                }
            }
            post{
                success {
                    script{
                        echo "Post success slave2"
                    }
                }
            }
        }
    }
}
