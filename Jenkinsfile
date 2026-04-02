pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/a2000kki-hub/akash.git',
                    credentialsId: '4914fa25-90d7-4efa-ab3e-fabbad4e02eb'
            }
        }

        stage('Build') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying to server'
            }
        }
    }
}
