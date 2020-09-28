pipeline{
    agent {
        label 'redhat'
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

            steps {
                sh 'mvn -DskipTests clean install'
                echo "In Build Stage"
            }
        }
    }
}