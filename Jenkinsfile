pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-11-slim'
      args 'added container'
    }

  }
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
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}