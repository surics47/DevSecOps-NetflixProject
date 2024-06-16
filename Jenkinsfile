pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git repository
                git branch: 'main', url: 'https://github.com/surics47/DevSecOps-NetflixProject.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install'  // Example command to install dependencies
                sh 'npm run build'  // Example command to build the project
            }
        }
        
        stage('Test') {
            steps {
                sh 'npm test'  // Example command to run tests
            }
        }
    }
    
    post {
        success {
            echo 'CI/CD pipeline completed successfully!'
            // Additional success post-build actions if needed
        }
        failure {
            echo 'CI/CD pipeline failed!'
            // Additional failure post-build actions if needed
        }
    }
}

