pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/JulyusIvan/ci-cd-automate.git'
            }
        }
        stage('Install Dependencies') {
            steps {
             
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
         
                bat 'pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Flask app...'
               
            }
        }
    }
}