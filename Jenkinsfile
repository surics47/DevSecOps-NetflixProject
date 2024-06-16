pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git repository
                git 'https://github.com/surics47/DevSecOps-NetflixProject.git'
            }
        }
        
        stage('Build') {
            steps {
                // Install dependencies and build your project
                sh 'npm install'  // Replace with your package manager command if different
                sh 'npm run build'  // Replace with your build command
            }
        }
        
        stage('Test') {
            steps {
                // Run tests (if applicable)
                sh 'npm test'  // Replace with your test command
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
