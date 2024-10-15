pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Specify the branch 'main' explicitly
                git branch: 'main', url: 'https://github.com/affaq-baig/cloud-computing-fyp.git'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the application using Docker Compose
                    sh 'docker-compose down && docker-compose up -d' 
                }
            }
        }
    }

}