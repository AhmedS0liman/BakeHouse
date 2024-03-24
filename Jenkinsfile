
pipeline {
    agent { label 'BakeHouseAgent' }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker login -u ${DOCKER_USER} -p ${DOCKER_PASS}'
                    sh 'docker build -t ahmeds0liman/back_housee:v2 .'
                    sh 'docker push ahmeds0liman/back_housee:v2'
                }
            }
        }
    }
}

