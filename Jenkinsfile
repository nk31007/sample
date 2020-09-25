pipeline {
  environment{
    JAVA_TOOL_OPTIONS="-Duser.home=/home/jenkins"
  }
  agent{
    dockerfilr {
      label redhat
      args '-v /tmp/maven:/home/jenkins/.m2 -e MAVEN_CONFIG=/home/jenkins/.m2'
    }
    }
    stages{
      stage("MavenBUILD")
      {
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