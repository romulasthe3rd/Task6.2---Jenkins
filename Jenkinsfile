pipeline{
    agent any
    stages
        {
    
    stage('Build') 
        {
            steps 
            {
                //Building the code using maven automation tool
                echo  "Building program using Maven automation tool"
                  
            }
        }

   stage('Unit and Integration Tests')
        {
            steps 
            {
                //running the Unit and Integration Tests
                echo "Unit and Integration Tests running..."
            }
            post
            {
                //If it fails it will send a failed comfirmation email to the address provided
                failure 
                {
                    mail to: "rom.frd19@gmail.com",
                        subject: "The Unit and Integration Tests has failed...",
                        body: "Unfortunately, the Unit and Integration Tests has failed. Please fix issues."
                        attachLog: true
                }
                //If it Succeeds it will send a Succeeded comfirmation email to the address provided
                success 
                {
                    mail to: "rom.frd19@gmail.com",
                        subject: "The Unit and Integration Tests has succeeded!",
                        body: "Fortunately, the Unit and Integration Tests has Succeeded!"
                        
                }


            }

        }
        stage('Code Analysis')
        {   
            steps
            {
                //Running code analysis using PMD
                 echo "Running code analysis using PMD"
            }

        }
        stage('Security Scan')
        {   
            steps 
            {
                //Running Security scan using Nessus
                echo "Running Security scan using Nessus"
            }
            post
            {   
                //If it fails it will send a failed comfirmation email to the address provided
                failure 
                {
                        mail to: "rom.frd19@gmail.com",
                        subject: "The Security Scan has failed...",
                        body: "Unfortunately, the Security Scan has failed. Please fix issues."
                        
                }
                //If it Succeeds it will send a Succeeded comfirmation email to the address provided
                success 
                {
                        mail to: "rom.frd19@gmail.com",
                        subject: "The Security Scan has succeeded!",
                        body: "Fortunately, the Security Scan has Succeeded!"
                        
                }
            
            }
            
        }
       
        stage('Integration Tests on Staging')
        {
            //Running the integration tests on staging
            steps
            {
                echo "Integration Tests on Staging running..."
            }
        }

        stage('Deploy to Production')
        {
            //Running the Deploy to Production using the AWS EC2 instace
            steps{
                echo"Deploy to Production server using AWS EC2 instance running..."
            }
        }    

        }
}

