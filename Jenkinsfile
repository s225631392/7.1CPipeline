// Auto-trigger demo recording
pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compile and package source code into a deployable artifact'
                echo 'Tool: Maven (build automation tool for Java projects)'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Run unit tests to verify individual functions, then integration tests to check components work together'
                echo 'Tools: JUnit for unit tests, Selenium for integration tests'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analyse source code for quality issues, code smells, and adherence to coding standards'
                echo 'Tool: SonarQube (static code analysis platform)'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scan code and dependencies for known security vulnerabilities (CVEs)'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Deploy the built application to a staging environment that mirrors production'
                echo 'Tool: AWS EC2 instance (cloud-based virtual server for staging)'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Run end-to-end tests against the staging deployment to verify behaviour in a production-like environment'
                echo 'Tools: Postman for API testing, Selenium for browser-based testing'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Deploy the verified application to the live production environment for end users'
                echo 'Tool: AWS EC2 instance (cloud-based production server)'
            }
        }
    }
}
