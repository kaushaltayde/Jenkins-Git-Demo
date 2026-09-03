   pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Source code checked out successfully!'
                echo 'Build executed successfully!'
            }
        }

        stage('Run') {
            steps {
                echo 'Project executed successfully!'
            }
        }
    }

    post {
        success {
            emailext(
                subject: "Jenkins Build SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: """
                    <h2>Build Successful</h2>
                    <p>Job: ${env.JOB_NAME}</p>
                    <p>Build Number: ${env.BUILD_NUMBER}</p>
                    <p>The Jenkins build completed successfully.</p>
                """,
                to: "kaushaltayde100@gmail.com"
            )
        }

        failure {
            emailext(
                subject: "Jenkins Build FAILED: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: """
                    <h2>Build Failed</h2>
                    <p>Job: ${env.JOB_NAME}</p>
                    <p>Build Number: ${env.BUILD_NUMBER}</p>
                    <p>The Jenkins build has failed.</p>
                """,
                to: "YOUR_EMAIL@gmail.com"
            )
        }
    }
}
