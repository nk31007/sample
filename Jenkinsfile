pipeline {
    agent {
        node {label 'redhat'}
        }
        options {
            timestamps()
        }
        environment {
            pom = readMavenPom file: 'pom.xml'
            IMAGE = pom.getArtifactId
            VERSION=pom.version
        }

    stages {
        stage("BUILD") {
            agent {
                docker {
                    reuseNode true
                    image 'maven:3.5.0-jdk-8'
                }
            }
            steps {
                withMaven(){
                    sh 'mvn clean package'
                }
            }
            post {
                success {
                    archiveArtifacts(artifacts: '**/target/*.jar', allowEmptyArchive: true)
                }
            }
        }
        }

}