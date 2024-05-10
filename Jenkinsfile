pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout Terraform code from repository
                git 'https://github.com/your-terraform-repo.git'
            }
        }
        stage('Terraform Init') {
            steps {
                // Initialize Terraform
                sh 'terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                // Generate Terraform plan
                sh 'terraform plan -out=tfplan'
            }
        }
        stage('Terraform Apply') {
            steps {
                // Apply Terraform changes
                sh 'terraform apply -auto-approve tfplan'
            }
        }
    }
}
