pipeline {
    agent any
    stages {
        stage('php build'){
           steps {
               archiveArtifacts artifacts: '*' , fingerprint: true , followSymlinks: false , onlyIfSuccessful: true
               sh 'docker build -t meghags17/php_final .'
               sh 'docker run  -d meghags17/php_final'
				}
			}
		}
	}

