pipeline {
    agent any

    environment {
        IMAGE_NAME = "hema3507/online-ticket-app:latest"
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Hema3507/OnlineTicketPlatform-BMS.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {

                    sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
                    sh 'docker push $IMAGE_NAME'
                }
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 --name online-ticket-container $IMAGE_NAME || true'
            }
        }

    }
}
