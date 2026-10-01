pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                git branch: 'main',
                    url: 'https://github.com/madhunisha-dev/milestoree.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'C:\\Users\\madhu\\AppData\\Local\\Programs\\Python\\Python312\\python.exe py_compile app.py'
                echo 'Build successful: app.py compiled with no syntax errors'
            }
        }

        stage('Send Notification') {
            steps {
                echo 'EMAIL WOULD BE SENT'
                echo "To: student@example.com"
                echo "Subject: Build Notification: ${env.JOB_NAME} #${env.BUILD_NUMBER}"
                echo "Build completed successfully!"
                echo "Build URL: ${env.BUILD_URL}"
            }
        }
    }
}