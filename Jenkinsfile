pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'echo Build completed > build-output.txt'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Tests completed'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'build-output.txt', fingerprint: true
        }
    }
}
