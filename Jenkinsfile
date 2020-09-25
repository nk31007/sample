pipeline {
  environment{
    JAVA_TOOL_OPTIONS="-Duser.home=/home/jenkins"
  }
  agent {
     agent { dockerfile true }
    }
     }
    
    stages{
      stage("MavenBUILD")
      {
        agent {

        }
        steps{
        sh 'mvn -version'
        }
      }
    }
    post{
      always{
        cleanWS()
      }
    }
}