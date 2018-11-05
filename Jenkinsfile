pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        withMaven() {
          sh 'mvn clean install'
        }

      }
    }
  }
}