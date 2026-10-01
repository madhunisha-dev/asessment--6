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
                bat 'python -m py_compile app.py'
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