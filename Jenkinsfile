node {
    stage('Build') {
        echo "Build"
	sleep 5
    }
    stage('Test') {
        echo "Test"
	sleep 2
    }
}
node ('maven') {    
    stage('DeployDev') {
        echo "Deploy to Dev"
	sleep 5
    }
    stage('PromoteTest') {
        echo "Deploy to Test"
	sleep 5
    }
    stage('PromoteProd') {
        echo "Deploy to Prod"
	sleep 5
    }
}

    


