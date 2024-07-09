pipeline {
  agent any

  stages {
    stage('Check Mongo Status') { 
      steps {
        script {
          sh 'docker ps | grep "mongo" || true'  
          if [ $? -eq 0 ] ; then
            echo 'Starting Mongo...'
            sh 'docker-compose up -d' 
          else
            echo 'Mongo is already running!'
          fi
        }
      }
    }
  }
}
