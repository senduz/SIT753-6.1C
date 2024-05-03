pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project using Maven.'
                // Tool used: Maven
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests using JUnit and Selenium.'
                // Tools used: JUnit for unit testing, Selenium for integration testing
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code quality with SonarQube.'
                // Tool used: SonarQube
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scanning using OWASP ZAP.'
                // Tool used: OWASP ZAP
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment using Ansible.'
                // Deployment tool: Ansible
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment using curl and grep.'
                // Tools used: curl for HTTP requests, grep for response validation
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment using Ansible.'
                // Deployment tool: Ansible
            }
        }
    }
    post {
        always {
            mail to: "itsvgggd@gmail.com",
            subject: "Build Status: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
            body: "The build was ${currentBuild.currentResult}: Check console output at ${env.BUILD_URL}."
        }
    }
}
