pipeline {
    agent any

    stages {
        stage('Build') {
					agent {
						docker {
							image 'node:20.16.0-alpine'
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
							echo "1"
              ls -la /var/lib/jenkins/workspace/React
							echo "2"
              npm config get cache
							
						'''
          }
        }
    }
}
