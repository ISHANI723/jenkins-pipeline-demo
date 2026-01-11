pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building and packaging the application using Maven'
                bat 'mvn clean package'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code analysis stage'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security scan stage'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline succeeded'
        }
    }
}
