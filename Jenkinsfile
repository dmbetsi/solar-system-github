pipeline {
    agent {label: server-js}
	tools {
      nodejs 'NodeJS24'
    }

    stages {

        stage('check nodeJS') {
            steps {
                script {
                   sh "node -v"
				   sh "npm -v"
					
                }
            }
        }
		
	}
}