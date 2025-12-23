pipeline {
  agent any
 
  stages {
    stage('Checkout Code') {
      steps {
        git branch: 'main', url: 'https://github.com/sricharan109/cicd-Jen'
      }
    }
 
    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }
 
    stage('Start App with PM2') {
      steps {
        sh '''
          pm2 delete myapp || true
          pm2 start index.js --name myapp
          pm2 save
        '''
      }
    }
  }
}