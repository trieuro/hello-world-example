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
    stage('Result') {
      steps {
        junit '**/target/surefile-report/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
      }
    }
  }
}