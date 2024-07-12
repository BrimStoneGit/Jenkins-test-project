pipeline {
    agent {
        docker {
            image 'python:3.12.4-alpine3.20'
            alwaysPull true
            reuseNode false
        }
    }
    stages {
        stage('Write File') {
            steps {
                script {
                    // Define the file path within the workspace
                    def filePath = "${env.WORKSPACE}/output.txt"

                    // Content to write to the file
                    def content = "Hello, this is some sample data."

                    // Write the content to the file
                    writeFile file: filePath, text: content

                    echo "File written successfully at ${filePath}"
                }
            }
        }
        stage('Download File') {
            steps {
                script {
                    // URL of the file to download
                    def fileUrl = 'https://ash-speed.hetzner.com/100MB.bin'

                    // Define the file path within the workspace
                    def downloadFilePath = "${env.WORKSPACE}/100MB.bin"

                    // Download the file
                    new URL(fileUrl).withInputStream { inputStream ->
                        Files.copy(inputStream, Paths.get(downloadFilePath))
                    }

                    echo "File downloaded successfully at ${downloadFilePath}"
                }
            }
        }
    }
}
