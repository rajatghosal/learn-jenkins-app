pipeline {
    agent any

    stages {
        stage('Build') {
            agents{
                docker{
                    image 'node:18-alpine'
                    resuseNode true
                }
            }
            steps {
                sh '''
                echo ls -la 
                node --version
                npm --version
                npm ci 
                run npm build
                ls -la
                '''
            }
        }
    }
}
