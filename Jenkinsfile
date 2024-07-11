/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
        docker { 
            image 'python:3.12.4-alpine3.20'
            alwaysPull true
        } 
    }
    stages {
        stage('build') {
            steps {
                downloadFile()
                sh 'ls -la'
            }
        }
    }
}
