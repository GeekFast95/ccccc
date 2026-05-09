pipeline {
    agent any
    
    environment {
        APP_VERSION = '1.1.0'
        BUILD_ENV = 'production'
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Building version ${APP_VERSION}.."
                echo "Environment: ${BUILD_ENV}"
            }
        }
        stage('Test') {
            steps {
                echo "Testing version ${APP_VERSION}.."
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying version ${APP_VERSION}.."
            }
        }
    }
}
