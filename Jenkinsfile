pipeline {
    agent { label 'agent'}
    
    stages {
          
          failFast true
            parallel {
                stage('Build ac-server-build-dev') {
                    steps {
                            build job: "/appcircle-backend/ac-server-build/${env.BRANCH}", wait: true
                    }
                }
                stage('Build ac-server-build-master') {
                    steps {
                            build job: "/appcircle-backend/ac-server-build/${env.BRANCH}", wait: true
                    }
                }
            }
    }
}
