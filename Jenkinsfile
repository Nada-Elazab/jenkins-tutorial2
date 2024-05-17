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
                // Run the batch file
                bat '''
                @echo off
                REM List files in the current directory
                dir
                call running.bat
                '''
            }
        }
    }
}
