pipeline {
    agent any

    stages {
        stage('Cloner') {
            steps {
                git branch: 'main', url: 'https://github.com/ademaloui/devops.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Tests') {
            steps {
                sh 'mvn test'
            }
        }
    }
}