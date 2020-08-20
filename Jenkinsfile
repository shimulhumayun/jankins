//DECLARATIVE 
pipeline {
	agent any

	stages {
		stage('Build') {
			steps {
				echo "Build"
						}
		}

		stage("Test") {
			steps {
				echo "Test"

			}
		}
		stage("Intergration") {
			steps {
				echo "Intergration"
			}
		}

	}
	post {
		always {
			echo "I run always"
		}
		success {
			echo "I run when you're successful"
		}
	}

}