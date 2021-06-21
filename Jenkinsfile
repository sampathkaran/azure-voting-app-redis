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
                sh 'cd azure-vote'
                docker build -t jenkins-voting-image ~/azure-vote/Dockerfile
                docker images -a
                '''
                
            }
        }
    }
    
}
