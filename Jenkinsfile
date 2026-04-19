pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/VectorVirtuoso/tripcircle-devops.git'
            }
        }

        stage('Build Docker Images') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Deploy Containers') {
            steps {
                sh 'docker-compose down || true'
                sh 'docker-compose up -d'
            }
        }

    }
}