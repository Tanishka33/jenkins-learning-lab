pipeline {
    agent any
    stages {
        stage('Checkout Verification') {
            steps {
                echo 'Repository cloned successfully'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('Build') {
            steps {
                echo 'Build Stage'
                sh 'python3 --version || true'
            }
        }
        stage('Test') {
            steps {
                echo 'Test Stage'
            }
        }
    }
    post {
        always {
            echo 'Pipeline Finished'
        }
    }
}
