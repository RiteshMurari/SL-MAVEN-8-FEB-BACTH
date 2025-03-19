pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/RiteshMurari/SL-MAVEN-8-FEB-BACTH'
            }
        }
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn clean package'  // Linux/Docker
                    } else {
                        bat 'mvn clean package' // Windows
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn test'  
                    } else {
                        bat 'mvn test'
                    }
                }
            }
        }
    }
}
