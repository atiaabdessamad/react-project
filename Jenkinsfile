pipeline {
  agent any
  stages {
    stage('Stop') {
      steps {
        sh 'docker rm -f  react-front | exit 0'
      }
    }
    stage('Build container') {
      steps {
        sh 'docker build -t react-front ./my-todo-list'
      }
    }
    stage('Run container') {
      steps {
        sh '''docker run -d --name react-front --net=host react-front
'''
      }
    }
  }
}