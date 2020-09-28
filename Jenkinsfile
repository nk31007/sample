pipeline{
    agent {
        label 'redhat'
        }
        options {
            skipDefaultCheckout true
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
                git 'https://github.com/nk31007/sample.git'
                sh 'mvn -DskipTests clean install'
                echo "In Build Stage"
            }
        }
    }
}
