pipeline {
    agent any
    triggers {
       cron('* * * * *')
       }
       options {
       buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '1', numToKeepStr: '2')
        }

    stages {
        stage("BUILD"){
            options{
                timeout(time:30, unit:'SECONDS')
                retry(3)
                timestamps()
            }
            input{
                message "This is Docker stages"
                ok  'Continue'
                submitter 'i633184, bhanu, sri'
                parameters{
                   text(name:"NAME", defaultValue: 'i633184', description : "This is default description")
                }
            }
            steps {
                echo "sample pipeline script"
            }
        }
    }
}
