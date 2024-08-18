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
							npm --version
							whoami		
						'''
          }
        }
    }
}
