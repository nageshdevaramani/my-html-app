pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/nageshdevaramani/my-html-app'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-html-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker rm -f my-html-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name my-html-container my-html-app'
            }
        }
    }
}
