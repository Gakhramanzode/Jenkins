node {
    /* Requires the Docker Pipeline plugin to be installed */

    stage('Back-end') {
        docker.image('maven:3.8.7-eclipse-temurin-11').inside {
            sh 'mvn --version'
        }
    }

    stage('Front-end') {
        docker.image('node:16.13.1-alpine').inside {
            sh 'node --version'
        }
    }
}