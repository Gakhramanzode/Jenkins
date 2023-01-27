node {
    stage('Build') {
        sh 'make' 
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}