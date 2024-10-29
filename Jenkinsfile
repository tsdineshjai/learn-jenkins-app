pipeline {
    agent any

    stages {
        stage('build process of the app') {
            agent {
              docker {
                image "node:18-alpine"
                reuseNode true          
              }
            }
            steps {
                
                sh """ 
                  node --version
                  npm --version
                  ls -la
                  npm ci
                  npm run build
                  ls -la
                """
            }
        }
    }
}
