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

        stage('Deploy') {
            steps {
                bat 'echo Deploying project'
            }
        }
    }
}
