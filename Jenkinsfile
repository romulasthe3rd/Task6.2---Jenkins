pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                // Build the code using Maven
                sh 'mvn clean package'
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



