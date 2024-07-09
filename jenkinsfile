pipeline {
    agent any

    stages {
        stage('check') {
            steps {
                script {
                    docker ps | grep 'mongo'
                    if (docker ps | grep 'mongo' != null){
                       docker compose up -d
                    } else{
                        echo 'mongo is already running!'
                    }
                }

            }
                            

            
        }
    }
    
}
