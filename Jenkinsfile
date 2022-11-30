pipeline {
	
	agent any

	stages {
		stage("Fetch code") {
			steps {
				git branch: 'main', url: 'https://github.com/helpingpeopletolearn/sample-app.git'
			}
		}
		stage("Install Apache") {
			steps {
				sh 'sudo apt install apache2 -y'
			}
		}
		stage("Deploy Application") {
			steps {
				sh 'sudo cp -R * /var/www/html/'
			}
		}
	}
}
