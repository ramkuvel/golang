#!/usr/bin/env groovy

// this will start an executor on a Jenkins agent with the docker label
node {


  // Checkout the code from Github, stages allow Jenkins to visualize the different sections of your build steps in the UI
  stage('Checkout from GitHub') {
    // No special needs here, if your projects relys on submodules the checkout step would need to be different
    //git branch: 'master', url: 'https://github.com/ramkuvel/golang.git' 
	checkout scm
  }

  stage("Create binaries") {
	mkdir ./build
	mkdir ./build/golang
	cd ./build/golang
	
  }

  stage("Run Test") {
	go run man.go
  }
}