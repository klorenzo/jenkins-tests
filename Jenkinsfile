pipeline {
	agent any

	tools {
		nodejs 'NodeJS v11.14.0'
	}

	options {
		timeout(time : 2, unit: 'MINUTES')
	}

	stages {
		stage('Greetings') {
			steps {
				sh 'echo "Hi Kevin :)"'
			}
		}
		stage('Print NodeJS Version') {
			steps {
				sh 'node -v'
			}
		}
	}
}