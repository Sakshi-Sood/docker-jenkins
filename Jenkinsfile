pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "sakshisood004/docker-jenkins"
    }
    stages {
        stage ("Build Docker image") {
            steps {
                sh "docker build -t ${DOCKER_IMAGE} ."
            }
        }
        stage ("Push image") {
            steps {
                // In a real scenario, use withCredentials to login
                // sh "docker login -u $USER -p $PASS"
                sh "docker push ${DOCKER_IMAGE}"
                echo "Docker image pushed successfully."
            }
        }
    }
}