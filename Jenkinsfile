pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ashardevops5-wq/frontend-pipeline-demo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage - Static project, nothing to build.'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage - No tests, skipping.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage - Skipping, just marking success.'
            }
        }
    }
}
