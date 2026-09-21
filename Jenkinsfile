pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    bat 'echo Deployment attempt'
                }

                timeout(time: 1, unit: 'MINUTES') {
                    bat 'echo Health check'
                }
            }
        }
    }
}
