pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git 'https://github.com/saggurthisandeep/TomcatMavenApp.git'
      }
    }

    stage('build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

  }
  tools {
    maven 'Maven-3.9.8'
  }
  environment {
    env = 'stagging'
  }
}