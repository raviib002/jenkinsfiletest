pipeline {
    //agent { label 'devops' }
    environment {

    }

    stages {
        stage('Read Config File') {
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
        stage('Download Artifacts') {
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
        }
        
        stage('Generate DB Scripts') {
            steps {
                script {
                    if (4 == 4)
                    {
                    echo "Generate DB Scripts is 4"
                    }
                }
            }
        }
        stage('Package') {
            steps {
                script {
                    echo "Package is 5"
                }
            }
        }
        stage('Testing activity') {
            steps {
                step {
                    script {
                    echo "Testing activity step 1"
                    }
                }
                step {
                    script {
                    echo "Testing activity step 2"                
                    }
                }
                step {
                    script {
                    echo "Testing activity step 3"                
                    }
                }
                step {
                    script {
                    echo "Testing activity step 4"
                    }
                }
            }
         }
        stage('Exctracting and excluding') {
            steps {
                script {
                    if (1 == 1) {
                    echo "Exctracting and excluding is 1"
                    } else {
                    echo "Exctracting and excluding is not 1"                    
                    }
                }
            }
            steps {
                script {
                    echo "Exctracting and excluding is 2"
                }
            }
        }
    }
    post{
        success {
            script{
                echo "Post success 1"
            }
        }
    }
    cleanup {
        script{
            if (1 == 1) {
                echo "Cleanup 1"
            }
        }
    }
}

