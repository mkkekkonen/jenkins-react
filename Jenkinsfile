pipeline {
	agent any
	stages {
		stage('Build') {
			checkout scm
			powershell 'npm run build'
		}
		stage('Test') {
			powershell 'npm test'
		}
	}
}
