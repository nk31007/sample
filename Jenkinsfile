pipeline {
  environment{
    CODE="JAVA"
    ENV="PROD"
  }
  agent any
  stages {
    stage("BUILD"){
      options {
        timeout(time:5, unit:'SECONDS')
       
      }
      steps {
        echo "Deployment stage"
          input message: "Depply ${env.CODE} codebase to ${env.ENV}", ok: 'Deploy' 
      }
    }
  }
}