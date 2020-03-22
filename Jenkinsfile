pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh
                bat "docker-compose up -d hub chrome firefox"
            }
        }
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up book-flight-module-chrome book-flight-module_firfox"
            }
        }
        stage('Stop Grid'){
            steps{
                bat "docker-compose down"
            }
        }
    }
}
