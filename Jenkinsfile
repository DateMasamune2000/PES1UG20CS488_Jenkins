pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				sh "make"
				echo "build stage done"
			}
		}
		stage('Test') {
			steps {
				sh "./hello_exec"
				echo "test stage done"
			}
		}
		stage('Deploy') {
			steps {
				echo "deploy stage done"
			}
		}
	}

	post {
		failure {
			echo "something went wrong here fix it yourself"
		}
	}
}
