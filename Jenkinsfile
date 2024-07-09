pipeline {
  agent any
  
  stages {
        stage('Check Mongo Status') {
            steps {
                script {

                    if (sh(returnStatus: true, script: 'docker ps | grep "mongo"')) {
                        echo 'Mongo is already running!'
                        
                    } else {
                        echo 'Starting Mongo...'
                        sh 'docker-compose up -d'
                    }
                }
            }
        }
    }
}
