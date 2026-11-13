
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Downloading HTML source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Checking HTML project files'
                sh 'ls -la'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t mystudy .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}

