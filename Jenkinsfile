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
                echo "Build Started"
            }
        }

        stage('Test') {
            steps {
                echo "Testing Application"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Completed"
            }
        }
    }
}
