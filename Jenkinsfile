node {
    stage('Build') {
        sh 'make' 
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
    }
    stage('Test') {
        /* `make check` returns non-zero on test failures,
         * using `true` to allow the Pipeline to continue nonetheless
         */
        sh 'make check || true' 
        junit '**/target/*.xml' 
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}