pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh './gradlew assemble'
        pushToCloudFoundry(target: 'https://api.run.pivotal.io', organization: 'lightwave', cloudSpace: 'development', credentialsId: '40901bf5-ee6e-4f82-b1dd-f2eedcb134cd')
      }
    }
  }
}