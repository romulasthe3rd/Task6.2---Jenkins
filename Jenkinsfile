pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "building"
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
