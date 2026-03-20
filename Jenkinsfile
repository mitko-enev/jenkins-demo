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

stage('Archive') {
    steps {
        archiveArtifacts artifacts: 'target/*.jar'
    }
}