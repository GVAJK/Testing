pipeline {
	agent any
	tools {
		maven "Maven-3.6.3"
		jdk "JDK-11"
	}
	stages {
		stage ('Fetch the code') {
			steps {
				git branch: "main", url: "https://github.com/GVAJK/Testing.git"
			}
		}
		stage ('Build') {
			steps {
				sh "mvn install"
				
			}
		}
		stage ('Docker Build') {
			steps {
			sh 'docker build -t image${BUILD_BUMBER} .'
			}
		}
	}
}