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
                sh 'mvn clean package'
            }
        }


        stage('Test') {
            steps {
                echo "Testing Application"
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t myapp:v1 .'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Completed"
            }
        }
    }
}
