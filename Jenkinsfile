pipeline {
    agent {
        docker {
            label 'windows'
            image 'mcr.microsoft.com/powershell'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}