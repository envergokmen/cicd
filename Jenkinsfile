pipeline {
    agent { label 'agent'}
    stages {
          stage('Build ac-server-build-dev') {
               steps {
                   script {
                     env.FROM_TRIGGER=true
                   }
                     build job: "/appcircle-backend/ac-server-build", wait: false
                }
          }
                
       
    }
}
