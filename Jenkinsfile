pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "building"
            }
           post
                {
                success
                {
                    mail to: "rom.frd19@gmail.com"
                    subject: "Build Status Email"
                    body: "Build was successfull"
                }
                }
        }
    }
}
