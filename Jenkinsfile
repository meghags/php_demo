pipeline {
    agent any
    stages {
        stage('php build'){
           steps {
               archiveArtifact artifacts: '*' , fingerprint: true , followSymlinks: false , onlyIfSuccessful: true
               sh 'docker build -t meghags171/php_final .'
               sh 'docker run -p 3000:80 -d meghags171/php_final'
				}
			}
		}
	}

