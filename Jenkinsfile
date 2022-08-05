pipeline {
    agent {
        docker {
            image "maven:latest"
        }
    }

    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}