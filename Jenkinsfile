pipeline {
    agent any
    tools {
        maven 'Maven 3.8.5'
        jdk 'JDK 17'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Chiranthan04/allnew.git'
            }
        }
        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }
        stage('Test Report') {
            steps {
                junit '**/target/surefire-reports/*.xml'
            }
        }
    }
}
