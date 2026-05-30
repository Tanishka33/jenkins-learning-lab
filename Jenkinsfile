pipeline {
    agent {
        label 'ec2-agent'
    }

    stages {
        stage('Checkout Verification') {
            steps {
                echo 'Repository cloned successfully'
                sh 'pwd'
                sh 'ls -la'
                sh 'hostname'
                sh 'whoami'
                sh 'pwd'
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
                sh 'python3 test_app.py'
                sh 'pytest -v'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Finished'
        }
    }
}
