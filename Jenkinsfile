pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up"
            }
        }
        stage('Bring Grid down') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
    }
}