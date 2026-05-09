pipeline {
    agent any
    
    tools {
        maven 'Maven'  // Name must match exactly what's in Jenkins Tools configuration
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn --version'  // For Linux/Mac
                // bat 'mvn --version'  // For Windows, use this instead
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test'  // For Linux/Mac
                // bat 'mvn test'  // For Windows
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
