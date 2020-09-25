pipeline {
  agent any
  stages{
    stage("Build"){
      steps{
        echo "Hi"
      }
    
    }
    stage("TEST"){
      when {
        expression { echo "Hi"}
      }
    }
    stage("Deploy"){
      steps{
        echo "Hello Nageswara"
      }
    }
  }
}