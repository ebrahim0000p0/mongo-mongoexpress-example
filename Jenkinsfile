pipeline {
  agent any

  stages {
    stage('Check Mongo Status') {
      steps {
        script {
          sh 'docker ps | grep "mongo"'  

          if (sh(returnStatus: true, script: 'docker ps | grep "mongo"')) {
            echo 'Starting Mongo...'
            sh 'docker-compose up -d'
          } else {
            echo 'Mongo is already running!'
          }
        }
      }
    }
  }
}
