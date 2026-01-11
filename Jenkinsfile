pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK9'
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
