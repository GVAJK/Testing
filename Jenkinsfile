pipeline {
	agent any
	stages {
		stage ('Fetch the code') {
			steps {
				sh "git clone https://github.com/GVAJK/Testing.git"
				sh "git branch main"
			}
		}
		stage ('Build the package') {
			steps {
				sh "mvn install"
			}
		}
	}
}