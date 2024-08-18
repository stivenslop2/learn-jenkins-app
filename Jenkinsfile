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
							ls -la
							npm cache clean --force 
							sudo chown -R 989:986 "~/.npm"
							node --version
							npm --version
							npm install
							ls -la
						'''
          }
        }
    }
}
