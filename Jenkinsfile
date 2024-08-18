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
							echo "El directorio de caché de npm es: $(npm config get cache)"					
							ls -la
							node --version
							npm --version
							rm -rf node_modules
							npm install
							npm run build
							ls -la
						'''
          }
        }
    }
}
