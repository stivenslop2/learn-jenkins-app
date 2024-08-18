pipeline {
    agent any

    stages {
        stage('Build') {
					agent {
						docker {
							image 'node:20.16.0-alpine'
							reuseNode true
							args '-u 1000:1000'
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
