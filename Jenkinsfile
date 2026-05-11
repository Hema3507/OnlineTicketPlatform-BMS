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
                dir('bookmyshow-app') {
                    sh 'npm install'
                }
            }
        }

         stage('Build Application') {
            steps {
		dir('bookmyshow-app') {
                    sh 'npm run build'
                }
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
