pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Unit Test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('Package') {
      steps {
        sh 'mvn package -Dkiptest '
        echo 'package maven app'
        archiveArtifacts 'targets/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}