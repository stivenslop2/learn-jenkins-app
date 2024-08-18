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
							npm cache clean --force
							ls -la
							node --version
							npm --version
							echo "0"
							whoami
							echo "2"
              npm config get cache
							
						'''
          }
        }
    }
}
