pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/devops-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                sh 'docker tag devops-app YOUR_DOCKER_USERNAME/devops-app'
                sh 'docker push YOUR_DOCKER_USERNAME/devops-app'
            }
        }
    }
}