pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the application..."
                // Insert your build commands here
            }
        }
        
        stage('Test') {
            steps {
                echo "Running tests..."
                // Insert your test commands here
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploying to Staging..."
                // Insert your staging deployment commands here
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying to Production..."
                // Insert your production deployment commands here
            }
        }
    }

    post {
        failure {
            echo "The build failed. Please check the logs for more details."
            // You can add more actions here to notify you in case of failure
            // Example: send an email or a Slack message
            mail to: '2024tm93068@wilp.bits-pilani.ac.in', subject: 'Jenkins Build Failed', body: 'The build has failed. Please investigate.'
            // or send Slack notifications
            // slackSend channel: '#your-channel', message: 'Build failed!'
        }
        
        success {
            echo "The pipeline completed successfully!"
        }

        unstable {
            echo "The build is unstable. Some tests may have failed."
        }
    }
}
