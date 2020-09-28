pipeline{
    agent {
        label 'redhat'
        }
        tools {
                  git 'Default'
              }

    stages {
        stage("BUILD"){
            agent {
                docker{
                reuseNode true
                image 'maven:3.5.0-jdk-8'
                args '-v /root/.m2:/root/.m2'
                }
            }
            tools {
              git 'Default'
            } 

            steps {
                sh 'mvn -DskipTests clean install'
                echo "In Build Stage"
            }
        }
    }
}