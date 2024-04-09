pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AmruthaParwatikar/Testing.git'
            }
        }
 
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
 
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
 
    post {
        success {
            echo 'Build succeeded!'
 
        }
        failure {
            echo 'Build failed!'
        }
    }
}
