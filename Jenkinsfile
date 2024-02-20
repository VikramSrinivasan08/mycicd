pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        post{
      always{
         emailext  to: "vikrammano6@gmail.com",
                  subject: "Notification mail from Jenkins",
                  body: "CI/CD pipeline completed successfully.\n\nCheck the application"
                
                
        }
      
      }
    }
}
}
