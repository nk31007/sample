pipeline {
  agent any
  stages {
    stage("STAGE1"){
      steps{
        echo "Hello-Worl"
      }
    }
    stage("Always skip") {
      expression {
        echo "Should I run?"
        return false
      }
      }
      steps {
        echo "Hello-World"
      }
  
  }

}