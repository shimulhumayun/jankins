//DECLARATIVE 
pipeline {
	//agent any
	agent {docker { image 'maven:3.6.3'}}
	stages {
		stage('Build') {
			steps {
				echo "Build"
					sh 'mvn --version '
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