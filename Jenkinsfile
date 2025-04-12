pipeline {
    agent { label 'local-agent' }

    stages {
        stage('Build') {
            steps {
                echo 'Building the Java application...'
                sh 'javac src/HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh 'echo "Tests passed!"'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                sh 'echo "Staging deployed"'
            }
        }

        stage('Deploy to Production') {
            steps {
                input message: 'Approve deployment to production?'
                echo 'Deploying to production environment...'
                sh 'echo "Production deployed"'
            }
        }
    }

    post {
        failure {
            echo 'Build failed! Sending alert...'
        }
    }
}
