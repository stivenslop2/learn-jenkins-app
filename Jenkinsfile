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
							ls -la
							node --version
							npm --version
							whoami
              ls -la /var/lib/jenkins/workspace/React
              npm config get cache
						'''
          }
        }
    }
}
