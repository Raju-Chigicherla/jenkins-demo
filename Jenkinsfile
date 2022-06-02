pipeline {
	agent any
	environment {
		DATE = "May 02nd, 2022"
	}
	stages {
		stage("Env Variables") {
			environment {
				NAME = "Raju Chigicherla"
			}
			steps {
				echo "Today is ${env.DATE}"
                echo "My name ${env.NAME}"
				
				script {
					env.WEBSITE = "localhost"
				}
				echo "This is an example for ${env.WEBSITE}"
				
				withEnv(["TEST_VARIABLE=TEST_VALUE"]) {
					echo "The value of TEST_VARIABLE is ${env.TEST_VARIABLE}"
				}
				
				echo "The current build number is ${env.BUILD_NUMBER}"
				echo "Another method is to use \${BUILD_NUMBER}, which is ${BUILD_NUMBER}"
			}
		}
		stage("build") {
			steps {
				echo 'Building the application...'
			}
		}
		stage("test") {
			steps {
				echo 'Testing the application...'
			}
		}
		stage("deploy") {
			steps {
				echo 'Deploying the application...'
			}
		}
	}
}
