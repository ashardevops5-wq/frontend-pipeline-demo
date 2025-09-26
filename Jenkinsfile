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
                echo 'Starting live preview server...'
                sh '''
                  pkill -f "http.server" || true
                  cd $WORKSPACE
                  nohup python3 -m http.server 8081 &
                '''
                echo "Project live hai: http://192.168.88.94:8081"
            }
        }
    }
}
