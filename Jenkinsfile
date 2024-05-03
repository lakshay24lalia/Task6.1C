pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo "Building the code using maven"
                
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests using mvn tests"
                echo "Running integration tests using mvn integration-test"
                
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Analysing the Code using SonarQube"
            }
        }
        stage('Security Scan') {
            steps {
               echo "Security scan to identify any kind of vulnerablities"
              echo"Perform security scan using OWASP ZAP"
            }
        }
        stage('Deploy to Staging') {
            steps {
               echo "Deploying the command to staging server using AWS CodeDeploy"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running Integration tests on staging using mvn integration-test -Denvironment=staging"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deployment to Production Environment using AWS CodeDeploy"
            }
        }
    }
}