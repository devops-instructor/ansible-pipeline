pipeline {
    agent {
        docker {
            image 'alpine/ansible:2.21.0'
            args '-u root:root'
        }
    }
    environment {
        HOME = "${WORKSPACE}"
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }
    stages {
        stage('ansible') {
            steps {
                sh 'ansible --version'

                sshagent(credentials: ['amazon-linux-private-key']) {

                    // sh 'ansible server1:server2:server3 -i hosts -m ping -u ec2-user'

                    sh 'ansible groupA -i hosts -m ping -u ec2-user'

                }
            }
        }
    }
}