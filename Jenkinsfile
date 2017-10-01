#!/usr/bin/env groovy
@Library('shared-libraries') _

	
pipeline {
	
    agent {
        label 'java'
    }
    
    stages {
	 stage('init') {
            steps {
		def a = load 'jenkins.*'    
                def b = new a.JenkinsPipelineBootsrap()
                def builder =  b.createBuilder()              
            }
        }
        stage('clone') {
            steps {  
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
