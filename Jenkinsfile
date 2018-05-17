pipeline {
    agent { docker { image 'node:nodejs_10_1_0' } }
    stages {
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Lint') { 
            steps {
                sh 'npm run lint'
            }
        }
        stage('Test') { 
            steps {
                sh 'npm run e2e'
            }
        }
    }
}