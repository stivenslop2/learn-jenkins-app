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
							echo "$(ls -la /)"
							ls -la
							node --version
							npm --version
							npm install
							npm run build
							ls -la
						'''
          }
        }
    }
}
