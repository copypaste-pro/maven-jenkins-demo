pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/copypaste-pro/maven-jenkins-demo.git'
            }
        }

        stage('Build') {
    steps {
        dir('my-maven-project') {
            bat 'mvn clean compile'
        }
    }
}

stage('Test') {
    steps {
        dir('my-maven-project') {
            bat 'mvn test'
        }
    }
}

stage('Package') {
    steps {
        dir('my-maven-project') {
            bat 'mvn package'
        }
    }
}
