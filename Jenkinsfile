pipeline {
    agent { label 'agent'}
    
    stages {
          
            stage('Set Default Env')
            {
                steps{
                   setDefaultEnvironment()
                   sh 'printenv'
                }
            }
   
          failFast true
            parallel {
                stage('Build ac-server-build-dev') {
                    steps {
                            build job: "/appcircle-backend/ac-server-build/${env.BRANCH_NAME}", wait: true
                    }
                }
                stage('Build ac-server-build-master') {
                    steps {
                            build job: "/appcircle-backend/ac-server-build/${env.BRANCH_NAME}", wait: true
                    }
                }
            }
    }
}
