pipeline {
    agent {
        docker {
            image 'alpine/ansible:2.21.0'
            args '-u root:root'
        }
    }
    environment {
        DEV = 'true'
        // HOME = "${WORKSPACE}"
        // ANSIBLE_HOST_KEY_CHECKING = 'False'
        // JBOSS_CREDENTIALS = credentials('jboss-credentials')
    }
    stages {
        stage('ansible') {
            steps {
                sh 'ansible --version'

                // sh 'whoami'
                // sh 'env | sort'
                // sh 'ansible-inventory --list'


            }
        }
    }
}