pipeline{
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	//agent { docker { image 'node:13.8'}}

	tools{
		maven 'myMaven'
		dockerTool 'myDocker'
	}

	environment {
		dockerHome = 'myDocker'
		mavenHome = 'myMaven'
		PATH="/dockerHome/bin:mavenHome:$PATH" 
	}
	stages {
		stage('Build'){
			steps {
				sh 'mvn --version'
				sh 'docker version'
			}
		}
		stage('Test'){
			steps {
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps {
				echo "Integration Test"
			}
		}
	} 
	post {
			always{
				echo "Working"
			}
			success{
				echo "Success Working"
			}
			failure{
				echo "Failed to work"
			}
		}
}