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

        success {
            emailext(
                subject: "Jenkins Build SUCCESS ",
                body: "Build completed successfully.\nCheck Jenkins for logs.",
                to: "${EMAIL_RECIPIENT}"
            )
        }

        failure {
            emailext(
                subject: "Jenkins Build FAILED ",
                body: "Build failed.\nCheck Jenkins logs immediately.",
                to: "${EMAIL_RECIPIENT}"
            )
        }
    }
}

