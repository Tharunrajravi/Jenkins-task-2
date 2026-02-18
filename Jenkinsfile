pipeline {
    agent any

    environment {
        EMAIL_RECIPIENT = "tharunrajravi440@gmail.com"
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Tharunrajravi/Jenkins-task-2.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build Started..."
                sh 'python3 app.py'
                echo "Build Completed."
            }
        }
    }

    post {
        always {
            emailext(
                subject: "Jenkins Build Notification 🚀",
                body: """
Build Status: ${currentBuild.currentResult}
Job Name: ${env.JOB_NAME}
Build Number: ${env.BUILD_NUMBER}
Build URL: ${env.BUILD_URL}
                """,
                to: "${EMAIL_RECIPIENT}"
            )
        }
    }
}
