pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git url: 'https://github.com/romulasthe3rd/Task6.2---Jenkins.git'

                // Build the code using Maven
                sh 'mvn clean package'
            }
           
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Hello"
            }
        }
        stage('Code Analysis') {
            steps {
                
            }
        }
        stage('Security Scan') {
            steps {
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                
            }
        }
        stage('Integration Tests on Staging') {
            steps {
             
            }
        }
        stage('Deploy to Production') {
            steps {
               
            }
        }
    }
}
