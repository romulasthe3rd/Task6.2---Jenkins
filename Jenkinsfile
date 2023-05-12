pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                // Checkout the source code from Git repository
                git url: 'https://github.com/romulasthe3rd/Task6.2---Jenkins.git'

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
