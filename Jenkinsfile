pipeline {
    agent any

    stages {
        stage('Display') {
            steps {
                sh 'echo "hello world"'
            }
        }
    

    
        stage('Docker-image-build') {
            steps {
                sh '''docker images  -a
                cd azure-vote
                docker build -t jenkins-voting-image .
                docker images  -a'''
                
            }
        }
    }
    
}
