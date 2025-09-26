pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<username>/frontend-pipeline-demo.git'
            }
        }

        stage('Test') {
            steps {
                echo "Running basic checks..."
                sh 'ls -lh'   // files check
                sh 'htmlhint index.html || true'
                sh 'stylelint "**/*.css" || true'
                sh 'eslint "**/*.js" || true'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment step (yahan server pe copy karna hoga agar chaho)"
            }
        }
    }
}
