pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/a2000kki-hub/akash.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying to server'
            }
        }
    }
}