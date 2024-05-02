pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/Users/manjinder/Desktop/Jenkinsfile'
        PRODUCTION_ENVIRONMENT = 'ManjinderSingh'
    }

    stages {
        stage('Build') {
            steps {
                echo "Building the code using Maven"
                // Implement build automation tool (e.g., Maven) here
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests"
                // Implement test automation tool for unit tests here
                echo "Running integration tests"
                // Implement test automation tool for integration tests here
            }
            post {
                success {
                    mail to: "mani28au@gmail.com",
                    subject: "Unit and Integeration Successfull",
                    body: "Stage 2 is successfully done"

                } 
                failure {
                   mail to: "mani28au@gmail.com",
                    subject: "Unit and Integeration Successfull",
                    body: "Stage 2 is successfully done"

                }
            }
        }
            stage('Code Analysis') {
            steps {
                echo "Performing code analysis"
                // Integrate code analysis tool (e.g., SonarQube) here
            }
        }
         stage('Security Scan') {
            steps {
                echo "Performing security scan"
                // Integrate security scanning tool (e.g., OWASP ZAP) here
            }
            post {
                success {
                    mail to: "mani28au@gmail.com",
                    subject: "Security Scan Success",
                    body: "Security Scan ran successfully"
                }
                failure {
                    mail to: "mani28au@gmail.com",
                    subject: "Security Scan Failure",
                    body: "Security Scan failed to run"                  
                }
            }
        }
        
    }
}
