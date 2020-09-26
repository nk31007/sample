pipeline {
  agent any
  stages {
    stage("BUILD"){
      options{
        timeout(time:5, unit: 'SECONDS')
      }
      steps{
        echo "STAGE BUILD STARTED"
        sleep 10
      }

    }

    stage("DEPLOY"){
      steps{
        echo "Hi This Nageswara an in Deployment STAGE"
      }
    }
  }
}