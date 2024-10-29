pipeline {
    agent any

    stages {
       stage('Clean Workspace') {
            steps {
                deleteDir() // Cleans the workspace before the build
            }
        }
        stage('build process of the app') {
            agent {
              docker {
                image "node:18-alpine"
                reuseNode true          
              }
            }
            steps {
                
                sh "npm install --verbose"
                sh "npm run build"
            }
        }
    }
}
