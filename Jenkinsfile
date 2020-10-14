pipeline {
	agent any
	stages {
		stage('Build') {
			script {
				try {
					echo '### BUILDING ###'
					checkout scm
					powershell 'npm run build'
				} catch (err) {
					echo err.getMessage()
				}
			}
		}
		stage('Test') {
			echo '### TESTING ###'
			powershell 'npm test'
		}
	}
}
