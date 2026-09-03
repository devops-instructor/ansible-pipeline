pipeline {
    agent {
        docker {
            image 'alpine/ansible:2.21.0'
        }
    }
    environment {
        HOME = "${WORKSPACE}"
    }
    stages {
        stage('ansible') {
            steps {
                // sh 'whoami'
                sh 'ansible --version'
            }
        }
    }
}