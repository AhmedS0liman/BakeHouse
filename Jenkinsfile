pipeline {
    agent { label 'BakeHouseAgent' }

    environment {
        DOCKER_REPO = 'ahmeds0liman/back_housee:v2'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker login -u ${DOCKER_USER} -p ${DOCKER_PASS}'
                    sh 'docker build -t ${DOCKER_REPO} .'
                    sh 'docker push ${DOCKER_REPO}'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'docker-compose -f docker-compose.yml up -d'
                }
            }
        }
    }
}
