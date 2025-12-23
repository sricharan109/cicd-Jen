pipeline {
    agent any
 
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/sricharan109/cicd-Jen.git'
            }
        }
 
        stage('Check Node Version') {
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }
 
        stage('Install Dependencies') {
            steps {
                echo 'Installing npm dependencies...'
                sh 'npm install'
            }
        }
 
        stage('Run App') {
            steps {
                echo 'Starting application...'
                sh 'nohup npm start > app.log 2>&1 &'
            }
        }
    }
}