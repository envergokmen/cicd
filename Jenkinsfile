pipeline {
    agent { label 'agent'}
    stages {
        
          stage('Build ac-server-build-dev') {
              
              script{
                 String fullPathBranch = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
                 env.BRANCH_NAME=fullPathBranch.substring(fullPathBranch.lastIndexOf('/') + 1, fullPathBranch.length()).trim()
              }
              
               steps {
                     sh "printenv"
                     build job: "/appcircle-backend/ac-server-build/$BRANCH_NAME", wait: false
                }
          }
                
       
    }
}
