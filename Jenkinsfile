pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'lock63', url: 'https://github.com/Pprashu-63/terra63.git'
            }
        }
        stage('Terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Terraform plan'){
            steps{
                sh 'terraform plan'
            }
        }
        stage('Terraform apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
        
    }
}