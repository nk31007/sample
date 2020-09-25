pipeline {
  environment {
    JAVA_TOOL_OPTIONS="-Duser.home=/var/maven"
  }
  agent {
    dockerfile {
      label 'redhat'
      args '-v /tmp/maven:/home/jenkins/.m2 -e MAVEN_CONFIG=/home/jenkins/.m2'
    }
    stages{
      stage("BUILD"){
        steps {
          sh 'mvn -version'
          sh 'ssh -V'
          sh 'mvn clean install'
        }
      }
    }
  }
}