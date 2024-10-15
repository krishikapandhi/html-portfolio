pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Example command: compile your code or build your app
                sh 'echo "Building application..."'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Example command: run tests
                sh 'echo "Running tests..."'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Example command: deploy your application
                // For example, using Docker
                sh 'docker build -t your-image-name .'
                sh 'docker run -d -p 8080:8080 your-image-name'
            }
        }
    }
}
