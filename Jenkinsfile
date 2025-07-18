pipeline {
    agent {label 'server-js'}
	tools {
      nodejs 'NodeJS24'
	  
    }

    stages {

        stage('check nodeJS') {
            steps {
                script {
                   sh "node -v"
				   sh "npm -v"
				   echo "hello world"
					
                }
            }
        }
		
		stage('install dependency') {
            steps {
                script {
				   sh "npm -v"
				   
					
                }
            }
        }
		
		stage('test') {
            steps {
                script {
				   sh "npm test"
				   
					
                }
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