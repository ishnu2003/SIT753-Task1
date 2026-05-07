pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compiling and packaging the application source code.'
                echo 'Tool: Maven - a build automation tool used for Java projects.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Running unit tests to verify individual components and integration tests to verify component interactions.'
                echo 'Tool: JUnit for unit tests, Selenium for integration tests.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analysing the code to ensure it meets industry standards and best practices.'
                echo 'Tool: Checkstyle - a static code analysis tool for Java that enforces coding standards.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scanning the code for known security vulnerabilities and CVEs.'
                echo 'Tool: OWASP Dependency-Check - identifies project dependencies with known vulnerabilities.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Deploying the packaged application to an AWS EC2 staging instance for pre-production testing.'
                echo 'Tool: AWS CLI - used to deploy application artifacts to an EC2 instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Running integration tests on the staging environment to verify the application behaves correctly in a production-like setup.'
                echo 'Tool: Selenium WebDriver - automates browser-based integration testing on the staging server.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Deploying the verified application to the live production AWS EC2 instance.'
                echo 'Tool: AWS CLI - automates deployment to the production EC2 instance.'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully. All 7 stages passed.'
        }
        failure {
            echo 'Pipeline failed. Please check the console output.'
        }
    }
}
