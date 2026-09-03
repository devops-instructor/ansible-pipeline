pipeline {
    agent {
        docker {
            image 'alpine/ansible:2.21.0'
            args '-u root:root'
        }
    }
    environment {
        // HOME = "${WORKSPACE}"
    }
    stages {
        stage('ansible') {
            steps {
                sh 'ansible --version'

                sshagent(credentials: ['amazon-linux-private-key']) {

                    sh 'ansible server1 -i hosts -m ping -u ec2-user'

                }
            }
        }
    }
}