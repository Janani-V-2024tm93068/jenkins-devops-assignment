pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Simple dummy test example
                sh 'java HelloWorld | grep "Hello, Jenkins!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Simulate deploy (you can copy to a folder or just print message)
                sh 'cp HelloWorld.class /tmp/' // or any dummy deploy step
            }
        }
    }
}
