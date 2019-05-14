pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
            sh label: '', script: 'sudo docker stop $(sudo docker ps -a -q) ; sudo docker system prune --all --force --volumes ; sudo docker-compose build ; sudo docker-compose up -d ; sudo docker exec testtesrver-php-fpm bash -c \'composer install\'; sudo chmod -R 777 .'       }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
