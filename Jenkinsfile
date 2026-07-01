pipeline {
    agent any

    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
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
