#!/usr/bin/env groovy
@Library('shared-libraries') _

	
pipeline {
	
    agent {
        label 'java'
    }
    
    
	
    stages {
	 
        stage('clone') {
            steps {
		def a = load 'jenkins.*'    
    def builder = a.JenkinsPipelineBootsrap
    def b =  builder.JenkinsPipelineBootstrap().createBuilder()    
                echo 'cloning...'
                git url: 'https://github.com/venkipat/javademo.git'
            }
        }
        stage('compile') {
            steps {
                echo "start compiling"
				sh script: 'javac HelloWorld.java'
				echo "stop compiling"
            }
        }
    }
}
