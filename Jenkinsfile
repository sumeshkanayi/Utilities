pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/sumeshkanayi/Webapp.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        sh 'mvn clean -f trucks/pom.xml'
      }
    }
  }
}