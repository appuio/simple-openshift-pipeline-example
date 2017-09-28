pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
    }
    stages {
        stage('Build') {
            steps {
                echo "Build"
            }
        }
	stage('Test') {
            steps {
                echo "Test"
            }
        }
	stage('DeployDev') {
            steps {
                echo "Deploy to Dev"
            }
        }
	stage('PromoteTest') {
            steps {
                echo "Deploy to Test"
            }
        }
	stage('PromoteProd') {
            steps {
                echo "Deploy to Prod"
            }
        }
    }
}
