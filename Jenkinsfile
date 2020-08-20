//DECLARATIVE 
pipeline {
	agent any
/* 	agent {
		docker { 
			image 'maven:3.6.3'
			}} */
	environment {
		dockerHome = tool 'myDocker'
		mavenHome  = tool 'myMaven'
		PATH	   = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Checkout') {
			steps {
				echo "Build"
				echo "$PATH"
				echo "$env.BUILD_NUMBER"
				echo "$PATH"
				}
		}
		stage("Compile") {
			steps {
				sh "mvn clean compile"
			}
		}

		stage("Test"){
			steps {
					sh "mvn test"
			}
		}
		stage("Intergration test"){
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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