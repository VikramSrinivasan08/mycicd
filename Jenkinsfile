pipeline {
  agent any
    post{
      always{
            sh 'docker rm -f mypycont'
            sh 'docker run --name mypycont -d -p 3000:5000 my-flask'
            catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
            mail  to: "yasmin@guvi.in",
                  subject: "Notification mail from Jenkins",
                  body: "CI/CD pipeline completed successfully.\n\nCheck the application"
                
                
        }
}
    }

