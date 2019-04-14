pipeline {
	agent any

	tools {
		nodejs 'node-11.14.0'
	}

	options {
		timeout(time : 2, unit: 'MINUTES')
	}

	stages {
		stage('Greetings') {
			sh 'echo "Hi Kevin :)"'
		}
		stage('Print NodeJS Version') {
			sh 'node -v'
		}
	}
}