pipeline {
    agent any
    
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                echo "Build automation tool: Maven"
            }
        }
        
        stage("Unit and Integration Tests") {
            steps {
                echo "Running tests..."
                echo "Test automation tool: Katalon"
            }
            post {
                success {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Unit and Integration Tests Passed",
                    body: "All tests have passed successfully!"
                }
                failure {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Unit and Integration Tests Failed",
                    body: "Some tests have failed. Please check the logs for more information."
                }
            }
        }
        
        stage("Code Analysis") {
            steps {
                echo "Analyzing code..."
                echo "Code analysis tool: SonarQube"
            }
        }
        
        stage("Security Scan") {
            steps {
                echo "Scanning code for security vulnerabilities..."
                echo "Security scan tool: Checkmarx"
            }
            post {
                success {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Security Scan Passed",
                    body: "No vulnerabilities detected!"
                }
                failure {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Security Scan Failed",
                    body: "Vulnerabilities found! Please check the logs."
                }
            }
        }
        
        stage("Deploy to Staging") {
            steps {
                echo "Deploying to staging..."
                echo "Staging server: AWS EC2"
            }
        }
        
        stage("Integration Tests on Staging") {
            steps {
                echo "Running integration tests on staging..."
            }
            post {
                success {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Staging Integration Tests Passed",
                    body: "Integration tests on staging have passed."
                }
                failure {
                    mail to: "upekshadilval@gmail.com",
                    subject: "Staging Integration Tests Failed",
                    body: "Integration tests on staging have failed. Please investigate."
                }
            }
        }
        
        stage("Deploy to Production") {
            steps {
                echo "Deploying to production..."
                echo "Production server: AWS EC2"
            }
        }
    }
}
