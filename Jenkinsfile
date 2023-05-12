pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "building"
                // Build the code using Maven
                
            }
           post
                {
                success
                {
                    mail to: "rom.frd19@gmail.com",
                    subject: "Build Status Email",
                    body: "Build was successfull"
                }
                }
        }

        stage("Unit and Integration Test"){
            steps{
                echo "Testing..."
                 sh 'mvn test' // runs all tests in the project using JUnit
                
                // start Selenium container using Docker
                sh 'docker run -d -p 4444:4444 selenium/standalone-chrome'
                // run integration tests using Selenium and TestNG
                sh 'mvn -Dtest=MyIntegrationTests test'
                // stop Selenium container
                sh 'docker stop $(docker ps -q -f "ancestor=selenium/standalone-chrome")'
            }
            }
        }

        stage("Code analysis"){
            steps{
                echo "Deploying..."
            }
        }

        stage("Security Scan"){
            steps{
                echo "Completing..."
            }
        }

        stage("Integration Tests on Staging"){
            steps{
                echo "Completing..."
            }
        }

        stage("Deploy to Production"){
            steps{
                echo "Completing..."
            }
        }
        
    }
}



