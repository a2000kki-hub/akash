pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/a2000kki-hub/akash.git',
                    credentialsId: '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'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app:latest .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker stop my-app || echo "No container running"'
                sh 'docker rm my-app || echo "No container to remove"'
                sh 'docker run -d --name my-app -p 3000:3000 my-app:latest'
            }
        }

        stage('Verify Deployment') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
