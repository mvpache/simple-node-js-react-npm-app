pipeline {
    agent {
        docker {
            image 'node:6-alpine' // download this image and run it in a seperate container
            args '-p 3000:3000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') { // appears on the ui
            steps { // commands to be executed
                sh 'npm install' 
            }
        }
         stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh' // see file to in jenkins folder to view steps
            }
        }
    }
}