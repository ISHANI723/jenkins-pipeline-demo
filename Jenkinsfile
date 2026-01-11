pipeline {
    agent any

    tools {
        maven 'Maven3'   // Maven configured in Jenkins (Manage Jenkins → Global Tool Configuration)
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building and packaging the application using Maven'
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests using Maven + JUnit'
                sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running static code analysis using SonarQube'
                // Example command (simulation if SonarQube is not configured)
                echo 'sonar-scanner would be executed here'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan using OWASP Dependency-Check'
                // Simulated security scan
                echo 'dependency-check.sh would scan for vulnerabilities'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to staging environment (AWS EC2)'
                // Simulated deployment
                echo 'scp target/app.jar ec2-user@staging-server:/app'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
                // Simulated integration testing
                echo 'Executing REST API tests using Postman / Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to production environment (AWS EC2)'
                // Simulated production deployment
                echo 'scp target/app.jar ec2-user@production-server:/app'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
