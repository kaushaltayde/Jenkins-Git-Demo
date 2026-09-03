pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/kaushaltayde/Jenkins-Git-Demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful!'
            }
        }

        stage('Run') {
            steps {
                echo 'Project executed successfully!'
            }
        }
    }
}