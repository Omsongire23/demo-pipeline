pipeline {
    agent any
    stages {

        stage('Checkout') {
            steps {
                echo "Checking out source code..."
            }
        }
        stage('Build') {
            steps {
                echo "Building project on branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Test') {
            steps {
                echo "Running tests on branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Finish') {
            steps {
                echo "Build completed successfully for ${env.BRANCH_NAME}"
            }
        }
    }
    post {
        success {
            echo "Build Success!"
        }
        failure {
            echo "Build Failed!"
        }
    }
}
