pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'YOUR_GITHUB_REPOSITORY_URL'
            }
        }

        stage('Build') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java HelloWorld'
            }
        }
    }
}