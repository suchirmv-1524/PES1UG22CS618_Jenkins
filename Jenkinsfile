pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG22CS618.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output' 
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
