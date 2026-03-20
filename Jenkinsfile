pipeline {
    agent {
        docker {
            image 'maven:3.9.9-eclipse-temurin-21'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
    
    post {
        success {
            echo '🎉 Build successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}