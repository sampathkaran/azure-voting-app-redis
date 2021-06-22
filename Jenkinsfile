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

        stage('push image to dockerhub') {
            steps {
                
                echo "workspace is $WORKSPACE"
                dir('$WORKSPACE/azure-vote') {
                // some block
                script {
                // some block
                docker.withRegistry('https://hub.docker.com/', 'Dockerhub') {
                def customImage = docker.build("voting-app:${env.BUILD_ID}")

               /* Push the container to the custom Registry */
                customImage.push()
    }    
}
}
                
            }
            
        }

         
    }
    
}
