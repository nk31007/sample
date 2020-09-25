pipeline {
  agent{
    dockerfilr {
      label docker
      args '-v /tmp/maven:/home/jenkins/.m2 -e MAVEN_CONFIG=/home/jenkins/.m2'
    }
    }
    stages{
      stage("MavenBUILD"){
        sh 'mvn -version'
      }
    }
    post{
      always{
        cleanWS
      }
    }
}