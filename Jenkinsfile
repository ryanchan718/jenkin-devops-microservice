pipeline{
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	//agent { docker { image 'node:13.8'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH="/dockerHome/bin:mavenHome:$PATH" 
	}
	stages {
		stage('Build'){
			steps {
				sh 'mvn --version'
				sh 'docker version'
				//sh 'node --version'
				// echo "Build"
				// echo "PATH - $PATH"
				// echo "BUILD_NUMBER - $env.BUILD.NUMBER"
				// echo "BUILD_ID - $env.BUILD.ID"
				// echo "JOB_NAME - $env.JOB_NAME"
				// echo "BUILD TAG - $env.BUILD_TAG"
				// echo "BUILD URL - $env.BUILD_URL"
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