pipeline {
    agent none
    stages {
        stage('Read Config File') {
            agent { label 'slave1' }
            steps{
                script {
                    if(1 == 1){
                    echo "read config file is 1"
                    sh("mkdir test111111111")
                    sh("touch test111111111/test11.txt")
                    sh("echo 'test11' >> test111111111/test11.txt")
                    sh("echo 'test1111' >> test111111111/test11.txt")                    
                    sh("touch test111111111/test1111.txt")
                    sh("echo 'test1111' >> test111111111/test1111.txt")
                    sh("echo 'test111111' >> test111111111/test1111.txt")
                    sh("tar -cvzf test1111.tar.gz test111111111/")
                    }
                    else
                    {
                    echo "read config file is not 1"
                    sh("mkdir test222222222")
                    sh("touch test222222222/test22.txt")
                    sh("echo 'test22' >> test222222222/test22.txt")
                    sh("echo 'test2222' >> test222222222/test22.txt")                    
                    sh("touch test222222222/test2222.txt")
                    sh("echo 'test22' >> test222222222/test2222.txt")
                    sh("echo 'test2222' >> test222222222/test2222.txt")                    
                    sh("tar -cvzf test2222.tar.gz test222222222/")
                    }
                }
            }
        }
        stage('Download Artifacts') {
            agent { label 'slave1' }
            steps{
                script {
                    if (1 == 1)
                    {
                    echo "Download Artifacts is 1 and extracting the tar11 file"
                    sh("mkdir abcd1234")
                    sh("mv test1111.tar.gz abcd1234/")
                    sh("tar -xvzf test1111.tar.gz -C abcd1234")
                    }
                    else
                    {
                    echo "Download Artifacts is not 1 and extracting the tar22 file"
                    sh("mkdir wxyz6789")
                    sh("mv test2222.tar.gz wxyz6789/")
                    sh("tar -xvzf test2222.tar.gz  -C wxyz6789")
                    }
                }
            }
        }       
        stage('Testing activity') {
            agent { label 'slave2' }
            steps{
                script {
                    echo "Testing activity step 1"
                }
            }
        }
        stage('Exctracting and excluding') {
            agent { label 'slave2' }
            steps{
                script {
                    echo "Exctracting and excluding is not 1"                    
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
