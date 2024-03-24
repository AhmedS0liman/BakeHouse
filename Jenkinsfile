
pipeline {
    agent { label 'BakeHouseAgent' }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker login -u ahmed.soliman241998@gmail.com -p 241998Ahmed'
                    sh 'docker build -t ahmeds0liman/back_housee:v2 .'
                    sh 'docker push ahmeds0liman/back_housee:v2'
                }
            }
        }
    }
}

