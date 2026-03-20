pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Maven build...'
                sh 'mvn clean package'
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