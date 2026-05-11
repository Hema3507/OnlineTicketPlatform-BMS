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

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

         stage('Build Application') {
            steps {
                sh 'npm run build'
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
