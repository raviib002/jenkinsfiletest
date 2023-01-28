pipeline {
    agent { label 'slave1' }
    environment {
        NEXUS_URL = 'https://nexus.cfrm.dev.local/repository'
        NEXUS_CREDS = credentials('nexus-creds')
        GIT_CREDS = credentials('CFRMGit-jenkins-svc')
        //#########################//
        INSTALLATION_PATH = '/home/deployment_scripts'
        SED_VAR = '        <Valve className="com.intellinx.authenticators.TenantIdMergedToUserNameValve" landingPage="/" disableProxyCaching="false" /> \n </Context>'
        SED_VAR1 = 'cloud.new_user.concatenate_tenant_automatically=true'
        IC_FOLDER = '/opt/ic'
        HOST_NAME = 'IL02VLDEVOPS5001.cfrm.dev.local'
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
            steps{
                script {
                    echo "Package is 5"
                }
            }
        }
        stage('Testing activity') {
            agent { label 'slave2' }
            steps {
                script {
                    echo "Testing activity step 1"
                }
            }
        }
        stage('Exctracting and excluding') {
            steps{
                script {
                    echo "Exctracting and excluding is not 1"                    
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
}
