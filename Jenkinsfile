pipeline {
  environment{
    CODE="JAVA"
    ENV="PROD"
  }
  agent any
  stages {
    stage("BUILD"){
      options {
        timeout(time:5, unit:'SECONDS'){
          input message: "Depply ${env.CODE} codebase to ${env.ENV}, ok: 'Deploy' "
        }
      }
      steps {
        echo "Deployment stage"
      }
    }
  }
}