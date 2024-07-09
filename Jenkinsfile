pipeline {
  agent any
  
  stages {
        stage('Check Mongo Status') {
            steps {
                script {
                    dir("/home/ebrahim/depi/trydocker/mongo-mongoexpress-example"){
                    if (sh (returnStatus: true, script: "docker ps | grep 'mongo' > /dev/null")  == 0) {
                        echo 'Mongo is already running!'
                        
                    } else {
                        echo 'Starting Mongo...'
                        sh 'docker compose up -d '
                    }
                }
                }
            }
        }
    }
}
