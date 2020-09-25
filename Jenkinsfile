pipeline {
 
  agent {
     agent { dockerfile true }
    }
     
    
    stages{
      stage("MavenBUILD")
      {
        steps{
        sh 'mvn -version'
        }
      }
    
    post{
      always{
        cleanWS()
      }
    }
}