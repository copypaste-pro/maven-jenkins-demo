pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/copypaste-pro/maven-jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
