pipeline {
    agent any

    stages {
        stage('Build') {
					agent {
						docker {
							image 'node:20.16.0-alpine'
							reuseNode true
							args '-u root --entrypoint /bin/sh -c "addgroup -g 986 jenkins && adduser -u 989 -G jenkins"'
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
