pipeline {
    agent any

    stages {
        stage('Build') {
					agent {
						docker {
							image 'node:18.20.4-alpine'
							reuseNode true
						}
					}
          steps {
            sh '''
							whoami
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
