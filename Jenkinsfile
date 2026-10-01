pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/madhunisha-dev/milestoree.git'
            }
        }

        stage('Build') {
            steps {
                bat 'C:\\Users\\madhu\\AppData\\Local\\Programs\\Python\\Python312\\python.exe py_compile app.py'
                echo 'Build stage passed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}