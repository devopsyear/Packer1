pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Initialize Packer') {
            steps {
                sh 'packer init aws-ami-v1.pkr.hcl'
            }
        }
        stage('Build AMI') {
            steps {
                sh 'packer build aws-ami-v1.pkr.hcl'
            }
        }
    }
}
