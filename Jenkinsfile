pipeline {
    agent any

    stages {

        stage('Check Docker') {
            steps {
                sh 'docker ps'
            }
        }

        stage('Run Test Container') {
            steps {
                sh 'docker run -d -p 8082:80 nginx'
            }
        }
    }
}
