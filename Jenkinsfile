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
			sh "./hello_cpp"
			echo "test stage done"
		}
		stage('Deploy') {
			echo "deploy stage done"
		}
	}

	post {
		failure {
			echo "something went wrong here fix it yourself"
		}
	}
}
