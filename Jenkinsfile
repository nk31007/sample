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
      steps{
        echo "in TEST stage"
      }
    }
    stage("Deploy"){
      steps{
        echo "Hello Nageswara"
      }
    }
  }
}