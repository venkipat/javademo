#!/usr/bin/env groovy

import jenkins.*
	
pipeline {
	
    agent {
        label 'java'
    }
	
    @Library('shared-libraries') _
    def builder = new jenkins.JenkinsPipelineBootstrap().createBuilder()
	
    stages {
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
