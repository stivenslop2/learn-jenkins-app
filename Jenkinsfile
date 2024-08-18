pipeline {
    agent any

    stages {
				stage('Pre-Build') {
          steps {
						cleanWs()
            sh '''
							echo "PERMISSIONS"
						'''
          }
        }
        stage('Build') {
					agent {
						docker {
							image 'node:20.16.0-alpine'
							reuseNode true
						}
					}
          steps {
            sh '''
							ls -la
							node --version
							npm --version
							npm ci
							ls -la
						'''
          }
        }
    }
}
