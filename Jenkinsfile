pipeline {
    agent any

    tools {
        maven 'MAVEN_HOME'  // Ensure this matches your Jenkins Maven configuration
    }

    stages {
        stage('Welcome Stage') {
            steps {
                echo 'Welcome to Pipeline'
            }
        }

        stage('Clean Stage') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn clean'
                    } else {
                        bat 'mvn clean'
                    }
                }
            }
        }

        stage('Build Stage') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn install'
                    } else {
                        bat 'mvn install'
                    }
                }
            }
        }

        stage('Build Success') {
            steps {
                echo 'Build Success'
            }
        }

        stage('Finish Stage') {
            steps {
                echo 'Finish Stage'
            }
        }
    }
}
