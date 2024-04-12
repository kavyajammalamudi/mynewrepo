pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('version') {
            steps {
                sh 'python3 --version'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt' // Install dependencies from requirements.txt
            }
        }

        stage('build') {
            steps {
                sh 'python3 methods.py'
                sh 'python3 pandas.py'
            }
        }
    }
    post {
        always {
            // Clean up any resources if needed
        }
    }
}

