pipeline{
    agent any
    environment {
        MASTER_IP = '192.168.56.70'
        JOIN_COMMAND = ''
    }
    stages{
        stage('Git Checkout Backstage') {
            steps {
                script {
                    git branch: 'master',
                        credentialsId: 'github-cred',
                        url: 'https://github.com/letuyenuit/backstage.git'
                }
            }
        }
        stage('Install Helm'){
            
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}