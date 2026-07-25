pipeline {
    agent any
    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['staging', 'production'],
            description: 'Select deployment environment'
        )
    }
    stages {
        stage('Build') {
            steps {
                echo "Building Application"
            }
        }
        stage('Test') {
            steps {
                echo "Running Tests"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
    post {
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline execution failed!"
        }
    }
}
