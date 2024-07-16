@Library('build-libraries') _

/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
        docker { 
            image 'python:3.12.4-alpine3.20'
            alwaysPull true
            reuseNode false
        } 
    }
    stages {
        stage('build') {
            steps {
                downloadFile("https://ash-speed.hetzner.com/100MB.bin", "testFile.bin")
            }
        }
    }
}
