pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')      // Build every 2 minutes
        pollSCM('H/1 * * * *')   // Poll SCM every 1 minute
    }

    stages {

        stage('Clone Repository') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'echo Build Successful'
            }
        }

        stage('Echo Build Status') {
            steps {
                echo "Build completed successfully!"
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '*.txt', fingerprint: true
            }
        }
    }
}
