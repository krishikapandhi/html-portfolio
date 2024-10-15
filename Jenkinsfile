pipeline {
    agent any

  environment {
        NODE_HOME = tool name: 'NodeJS', type: 'nodejs'
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }
    

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                git 'https://github.com/krishikapandhi/html-portfolio.git'
            }
        }
        stage('Check Node Version') {
                steps {
                    bat 'node -v' // This should print the Node.js version
                    bat 'npm -v'  // This should print the npm version
                }
            }

        stage('Install Dependencies') {
            steps {
                // Install npm dependencies
                bat 'npm install'
            }
        }
        stage('Run nodejs app') {
            steps {
                bat 'npm start '
            }
        }
               
    }
}

