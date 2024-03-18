pipeline {
    agent any
    stages {
        stage('Back-end') {
            agent {
                docker {
                    image 'maven:3.8.4-openjdk-17' // Updated Maven version with OpenJDK 17
                    args '-v $HOME/.m2:/root/.m2'
                }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                docker {
                    image 'node:14-alpine' // Updated Node.js version with Alpine Linux
                    args '-v $HOME/.npm:/root/.npm'
                }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
