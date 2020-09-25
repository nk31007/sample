pipeline {
  environment{
    JAVA_TOOL_OPTIONS="-Duser.home=/home/jenkins"
  }
  agent {
     dockerfile {
        args "-v /tmp:/tmp -p 8000:8000"
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