pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/almanyen/api-automation-framework.git'
            }
        }

        stage('Install Newman') {
            steps {
                bat 'npm install -g newman'
            }
        }

        stage('Run API Tests') {
            steps {
                bat 'newman run collections/api_tests.json'
            }
        }

    }
}