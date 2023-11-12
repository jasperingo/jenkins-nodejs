pipeline {
  agent { 
    node {
      label 'docker-agent-nodejs'
    }
  }
  triggers {
    pollSCM '* * * * *'
  }
  stages {
    stage('Build') {
      steps {
        echo "Building.."
        sh '''
        npm install
        '''
      }
    }
    stage('Test') {
      steps {
        echo "Testing.."
        sh '''
        node logger.js
        '''
      }
    }
    stage('Deliver') {
      steps {
        echo 'Deliver....'
        sh '''
        echo "doing delivery stuff.."
        '''
      }
    }
  }
}
