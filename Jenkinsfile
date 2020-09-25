pipeline {
  agent {
    docker {
        dockerfile true
        label 'redhat'
    }
}
   stages{
    stage("Build")
    {
      agent {
        dockerfile true
      }
      steps{
        echo "Hi Nageswara Rao"
      }
    }
  }
}