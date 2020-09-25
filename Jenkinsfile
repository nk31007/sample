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
        expression { return 0 }
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