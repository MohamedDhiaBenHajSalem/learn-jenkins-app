pipeline {
    agent any 

    stages{
        stage('Build') {

            agent{
                docker {
                    image 'node18-alpine'
                    reuseNode true
                }
            }


            steps {
                '''
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                ls -la
                '''
                
            }
        }
    }



}