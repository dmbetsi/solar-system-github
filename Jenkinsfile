pipeline {
    agent {label 'server-js'}
	tools {
      nodejs 'NodeJS24'
	  
    }

    stages {

        
		stage('install dependency') {
            steps {
                script {
				   sh "npm -v"
				   
					
                }
            }
        }
		stage('Check dependencies') {
            steps {

                // Vérifie les vulnérabilités (audit)
                sh 'npm audit --audit-level=critical || true'
            }
        }
		
		stage('check nodeJS') {
            steps {
                script {
                   sh "node -v"
				   sh "npm -v"
				   sh 'npx mocha --version'
					
                }
            }
        }
		
		
		stage('test') {
            steps {
                
				sh 'npm test'	
               
            }
        }
		
		stage('deploy') {
            steps {
                script {
				   sh "npm start"
				   
					
                }
            }
        }
	}
}