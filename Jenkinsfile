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

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-app:latest .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker stop my-app || echo "No container running"'
                bat 'docker rm my-app || echo "No container to remove"'
                bat 'docker run -d --name my-app -p 3000:3000 my-app:latest'
            }
        }

        stage('Verify Deployment') {
            steps {
                bat 'docker ps'
            }
        }
    }
}
