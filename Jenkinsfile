pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {

        stage('Clone') {
            steps {
                echo "Code Cloned Successfully"
            }
        }

        stage('Build') {
            steps {
                echo "Build completed Successfully"
            }
        }

        stage('Test') {
            steps {
                echo "Testing Successful"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Successful"
            }
        }
    }
}
