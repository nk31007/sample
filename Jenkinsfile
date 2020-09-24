pipeline {
  agent any
  parameters{
    booleanParam(defaultValue: false,description: "Simulate the Promotion", name: 'SIMULa')
  }
stages{
  stage("PROMOTE") {
    when {
      expression {
                    // only run when the current build number is odd
                    currentBuild.getNumber() % 2 == 1
                }
      steps {
        build job: currentBuild.getProjectName(), parameters: [
                    booleanParam(name: 'SIMUL', value: params.SIMUL)
        ]
      }
    }
  }
 }
}
