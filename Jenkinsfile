pipeline {
    agent any
    stages {
        stage ("Build Docker image") {
            steps {
                sh "docker build -t sakshisood004/docker_jenkins_project ."
            }
        }
        stage ("Push image") {
            steps {
                echo "Docker image pushed."
            }
        }
    }
}