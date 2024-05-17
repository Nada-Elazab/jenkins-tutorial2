pipeline {
    agent any
    
    environment {
        REPO_URL = 'https://github.com/Nada-Elazab/jenkins-tutorial2.git' // Replace with your repository URL
        BRANCH = 'main'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Pull the repository
                git branch: env.BRANCH, url: env.REPO_URL
            }
        }
        
        stage('Execute Script') {
            steps {
                // Ensure the script is executable
                sh 'chmod +x running.sh'
                
                // Execute the script
                sh './running.sh'
            }
        }
    }
}
