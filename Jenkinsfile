/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.12.4-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'wget https://ash-speed.hetzner.com/100MB.bin'
                sh 'ls -la'
            }
        }
    }
}
