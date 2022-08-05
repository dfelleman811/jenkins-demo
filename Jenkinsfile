pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
        stage("Deploy") {
            steps {
                sh "nohup mvn spring-boot:run &"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}