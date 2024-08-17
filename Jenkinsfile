pipeline {
    agent any

    stages {
        stage('Build') {
					agent {
						docker {
							image 'node:18-alpine'
							reuseNode true
						}
					}
          steps {
            sh '''
							npm cache clean -force
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
