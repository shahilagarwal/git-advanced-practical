node {

    stage('Clone Repository') {
        echo 'Cloning repository...'
    }

    stage('Build') {
        echo 'Building project...'
        sh 'echo Build Successful'
    }

    stage('Echo Build Status') {
        echo 'Build completed successfully!'
    }

    stage('Archive Artifacts') {
        archiveArtifacts artifacts: '*.txt', fingerprint: true
    }
}

