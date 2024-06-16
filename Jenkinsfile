pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git repository
                git 'https://github.com/surics47/DevSecOps-NetflixProject.git'
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git repository
                git branch: 'main', url: 'https://github.com/surics47/DevSecOps-NetflixProject.git'
            }
        }
        
        // Add more stages as needed (Build, Test, Deploy)
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
