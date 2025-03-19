pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'feature-login', url: 'https://github.com/RiteshMurari/SL-MAVEN-8-FEB-BACTH.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment stage - add actual deployment command here'
                // Example: sh 'mvn deploy'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
