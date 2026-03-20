pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Maven build...'
                bat 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Build SUCCESS'
        }
        failure {
            echo 'Build FAILED'
        }
    }
}