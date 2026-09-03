pipeline {
    agent {
        docker {
            image 'alpine/ansible:2.21.0'
        }
    }
    stages {
        stage('ansible') {
            steps {
                sh 'whoami'
                sh 'ansible --version'
            }
        }
    }
}