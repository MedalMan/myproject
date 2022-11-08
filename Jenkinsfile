pipeline{
	agent any;
	
	stages{
		stage('SCM Checkout'){
			steps{
				git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/myproject'
			}

		}
		stage('Build Docker Image'){
			steps{
				sh 'docker  login  -u "Rahi776" -p "Rahi@2002";'
				sh 'docker build -t Rahi776/test-1.0 .';
			}

		}
	}
}


