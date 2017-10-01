#!/usr/bin/env groovy

@Library('shared-libraries') _

import jenkins.*

def builder = new JenkinsPipelineBootstrap().createBuilder()
	
pipeline {
	
    agent {
        label 'java'
    }
	
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
