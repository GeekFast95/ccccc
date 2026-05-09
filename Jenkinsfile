pipeline {
    agent any
    
    parameters {
        string(name: 'VERSION', defaultValue: '1.1.0', description: 'Version to deploy')
        choice(name: 'ENVIRONMENT', choices: ['development', 'staging', 'production'], description: 'Select environment')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests?')
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Building version ${params.VERSION}.."
            }
        }
        stage('Test') {
            when {
                expression {
                    params.executeTests == true
                }
            }
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying version ${params.VERSION} to ${params.ENVIRONMENT}"
            }
        }
    }
}
