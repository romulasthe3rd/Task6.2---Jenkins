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

        stage("Test"){
            steps{
                echo "Testing..."
            }
        }

        stage("Deploy"){
            steps{
                echo "Deploying..."
            }
        }

        stage("Complete"){
            steps{
                echo "Completing..."
            }
        }
        
    }
}
