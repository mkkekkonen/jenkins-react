pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
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
		}
		stage('Test') {
			steps {
				echo '### TESTING ###'
				powershell 'npm test'
			}
		}
	}
}
