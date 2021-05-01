pipeline {
    agent any
    stages {
        stage('php build'){
           steps {
               archiveArtifacts artifacts: '*' , fingerprint: true , followSymlinks: false , onlyIfSuccessful: true
               sh 'docker build -t meghags17/php_final .'
               sh 'docker run -p 3000:80 -d meghags17/php_final'
				}
			}
		}
	}

