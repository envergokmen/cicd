pipeline {
    agent { label 'agent'}
    
    stages {
        
          stage('Build ac-server-build-dev') {
               steps {
                     build job: "/appcircle-backend/ac-server-build/${env.BRANCH_NAME}", wait: true
                }
          }
                
       
    }
}
