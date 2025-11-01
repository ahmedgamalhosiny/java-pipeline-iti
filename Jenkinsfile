pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Java project...'
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulating deployment...'
                bat 'echo Deploying application...'
            }
        }
    }

    post {
        success {
            echo ' Build and deployment succeeded!'
        }
        failure {
            echo ' Build or tests failed!'
        }
    }
}
