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
        expression { return 127 }
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