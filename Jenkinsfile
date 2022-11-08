pipeline{
	agent any;
	
	stages{
		stage('SCM Checkout'){
			steps{
				git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/myproject'
			}

		}
		stage('Build image'){
			dockerImage = docker.build("rahi776/node-app:latest")
		}
	}
}


