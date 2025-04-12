pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the application..."
                // Simulate build commands here
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Simulate test commands here
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploying to Staging..."
                sh 'mkdir -p staging && echo "Staging Build" > staging/index.html'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying to Production..."
                input message: "Promote to Production?", ok: "Yes, Deploy"
                sh 'mkdir -p production && echo "Production Build" > production/index.html'
            }
        }
    }

    post {
        failure {
            echo "The pipeline failed!"
        }
        success {
            echo "Pipeline completed successfully!"
        }
    }
}
