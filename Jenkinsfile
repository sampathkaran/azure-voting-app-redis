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
                sh 'docker images  -a '
                
                sh '''docker images  -a 
                docker build -t jenkins-voting-image ~/azure-vote/
                docker images -a
                '''
                
            }
        }
    }
    
}
