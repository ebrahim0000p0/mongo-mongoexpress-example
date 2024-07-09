pipeline {
    agent any

    stages {
        stage('check') {
            steps {
                script {
                   sh 'docker ps | grep "mongo"'
                    if (docker ps | grep 'mongo' != null){
                     sh 'docker compose up -d'
                    } else{
                        echo 'mongo is already running!'
                    }
                }

            }
                            

            
        }
    }
    
}
