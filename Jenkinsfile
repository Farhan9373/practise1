pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                echo "Cloning repository..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                bat "echo Build Successful > build.txt"
            }
        }

        stage('Echo Build Status') {
            steps {
                echo "Build completed successfully."
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'build.txt'
            }
        }
    }
}