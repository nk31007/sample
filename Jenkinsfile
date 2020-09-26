pipeline {
  agent {
    dockerfile {
      label 'redhat'
      args '-v /tmp/maven:/home/jenkins/.m2 -e MAVEN_CONFIG=/home/jenkins/.m2'
    }
  }
    environment {
    JAVA_TOOL_OPTIONS="-Duser.home=/home/jenkins"
  }
  tools {
  maven 'M3'
}
    stages{
      stage("BUILD"){
     /* timeout(activity: true, time: 200, unit: SECONDS){
      input{
            message "Press ok to continue"
	    submitter "nk31007"
	    parameters {
   	         string(name:'username', defaultValue: 'nk31007', description: 'Username of the user pressing Ok')
		} 
               }
	       }*/
         steps {
           timeout(activity: true, time: 200, unit: 'SECONDS') {
             input {
                    message "Press OK to Continue"
                    ok "Double okay"
                    submitter "i633184,nk31007,bhanu"
                    parameters {
                    string(name:"submitting guy", defaultValue: "bhanu",description: "Username of the guy pressing ok")
               }
             }

           }
	  echo "User: ${username} said ok." 
          sh 'mvn -version'
          sh 'ssh -V'
          sh 'mvn clean install'
        }
      }
    }
}
