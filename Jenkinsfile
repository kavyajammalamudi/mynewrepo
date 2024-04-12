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

        stage('build') {
            steps {
                sh 'python3 methods.py'
            }
        }
    }
}
