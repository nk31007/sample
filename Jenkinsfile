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
        expression { 5>2}
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