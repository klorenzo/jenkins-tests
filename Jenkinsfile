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
		stage('Build Other Job') {
			steps {
				build job: 'kl-parameterized', parameters: [string(name: 'ROOT_ID', value: '$BUILD_ID')], propagate: false, wait: false
			}
		}
		stage('List of Elements') {
			steps {
				sh 'ls -l'
			}
		}
		stage('Print NodeJS Version') {
			steps {
				sh 'node -v'
			}
		}
	}
}