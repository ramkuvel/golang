#!/usr/bin/env groovy

node {
	try {
	  // Checkout the code from Github, stages allow Jenkins to visualize the different sections of your build steps in the UI
	  stage('Checkout from GitHub') {
		// No special needs here, if your projects relys on submodules the checkout step would need to be different
		//git branch: 'master', url: 'https://github.com/ramkuvel/golang.git' 
		checkout scm
	  }

	  stage("Create binaries") {
		cd ./build	
	  }

	  stage("Run Test") {
		go run man.go
	  }
	}catch(ex){
		throw ex
	}
}