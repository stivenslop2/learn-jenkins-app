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
						  echo "CACHE"
							npm config get cache						
							ls -la
							node --version
							npm --version
							sudo npm ci
							sudo npm run build
							ls -la
						'''
          }
        }
    }
}
