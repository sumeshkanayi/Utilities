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
        parallel(
          "build": {
            sh 'ls'
            
          },
          "parallel1": {
            sh 'ls'
            
          }
        )
      }
    }
    stage('promote') {
      steps {
        input(message: 'enter your name', ok: 'yes')
      }
    }
    stage('deploy') {
      steps {
        writeFile(file: 'out.txt', text: 'hello')
      }
    }
    stage('print') {
      steps {
        sh 'ls'
        mail(subject: 'helo', body: 'haai')
        waitUntil() {
          build 'com.rxcorp.test'
        }
        
      }
    }
  }
}