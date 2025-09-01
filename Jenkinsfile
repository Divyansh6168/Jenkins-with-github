pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Divyansh6168/Jenkins-with-github.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage placeholder (no npm project found)"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests placeholder"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage placeholder"
            }
        }
    }
}
