pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/RiteshMurari/SL-MAVEN-8-FEB-BACTH/tree/feature-login'
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
