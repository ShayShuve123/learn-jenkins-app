pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'ls -la'
                sh 'npm --version'
                sh 'node --version'
                sh 'npm ci'
                echo 'Build app'
                sh 'npm run build'
            }
        }
    }
}
