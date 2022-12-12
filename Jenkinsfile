pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vastevenson/pytest-intro-vs.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/vastevenson/pytest-intro-vs.git'
                bat 'python --version'
            }
        }
        stage('Test') {
            steps {
                bat 'python3 -m pytest'
            }
        }
    }
}
