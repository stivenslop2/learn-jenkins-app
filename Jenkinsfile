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
							sudo chown -R 989:986 "/.npm"
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
