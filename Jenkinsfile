pipeline {
  agent any
  stages {

    stage("BUILD"){
      options{
        timestamps()
        timeout(time:5, unit:"SECONDS")
      }
      steps {
        echo "This is Nageswara Rao"
      }
    }
     stage("BUILDC") 
     {
       steps{
         echo "I am in BUILDC STAGE"
       }
     }
    }

  }
}