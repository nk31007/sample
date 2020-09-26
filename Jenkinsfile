pipeline {
  agent any
  stages {
   stage("STAGEA")  {
     options {
     timeout(time: 30, unit: 'SECONDS')
  }
  steps{
    echo "I am in stage A"
  }

  stage("stageB"){
    options {
      timestamps()
      }
    steps{
      echo "I am in STAGE-B"
    }  
  }

  }

  }
}