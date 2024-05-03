pipeline{
    agent any
    stages{
        stage("Build"){
        steps{
            echo "Building..."
            echo "Build automation tool: Maven"
        }
    }
        stage("Unit and Integration Test"){
        steps{
            echo"Running tests..."
            echo "Test automation tool: Katalon"
        }
        post{
            success{
                mail to: "upekshadilval@gmail.com",
                subject: "build status email",
                body: "build was successful!"
            }
        }
    }
        stage("Code analyse"){
            steps{
                echo "Analysing code..."
                echo "code analyse tool: SonarQube"
        }
    }
        stage("Security scan"){
            steps{
                echo "Analysing code..."
                echo "Security scan tool: Checkmarx"
        }
        post{
            success{
                mail to: "upekshadilval@gmail.com",
                subject: "build status email",
                body: "build was successful!"
            }
        }
    }
        stage("Integration Tests on Staging "){
            steps{
                echo "Testing stages..."
        }
    }
        stage("Deploy"){
            steps{
                echo "Deploying..."
                echo "Production server: AWS EC2"
        }
    }
        
        }
    }

