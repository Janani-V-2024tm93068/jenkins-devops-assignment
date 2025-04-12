pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // You can add actual build commands here if needed
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // You can add your testing framework commands here
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                bat '''
                if not exist staging (
                    mkdir staging
                )
                echo Staging Build > staging\\index.html
                '''
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                bat '''
                if not exist production (
                    mkdir production
                )
                echo Production Build > production\\index.html
                '''
            }
        }
    }

    post {
        success {
            echo 'The pipeline completed successfully!'
        }
        failure {
            echo 'The pipeline failed!'
        }
    }
}
