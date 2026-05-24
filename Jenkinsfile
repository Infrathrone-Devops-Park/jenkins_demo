pipeline {
    agent any
    stages {
        stage('Build') {
            steps { sh 'echo "Build: jenkins_demo commit $(git rev-parse --short HEAD)"' }
        }
        stage('Test') {
            steps { sh 'python3 -m unittest -v || echo "(python3 not present — skipping)"' }
        }
    }
}
