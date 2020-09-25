pipeline {
  agent {
    docker {
        dockerfile true
        label 'docker'
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