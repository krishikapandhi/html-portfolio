pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/krishikapandhi/html-portfolio.git'
            }
        }
        stage('Build') {
            steps {
                sh './build.sh'  // Replace with your build command
            }
        }
        stage('Test') {
            steps {
                sh './test.sh'  // Replace with your test command
            }
        }
        stage('Deploy') {
            steps {
                sh './deploy.sh'  // Replace with your deployment command
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            junit '**/target/test-*.xml'
        }
    }
}
