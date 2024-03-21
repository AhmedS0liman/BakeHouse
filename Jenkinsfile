pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker login -u ahmed.soliman241998@gmail.com -p 241998Ahmed'
                sh 'docker build -t back_house/web-image:latest . '
                sh 'docker push ahmeds0liman/back_house_image:latest'
            }
        }
    }
} 
