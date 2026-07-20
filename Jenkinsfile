pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build successful!"'
            }
        }

        stage('List files') {
            steps {
                sh 'ls -la'
            }
        }
    }
}
