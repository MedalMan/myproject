pipeline{
	agent any;
	
	stages{
		stage('SCM Checkout'){
			steps{
				git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/myproject'
			}

		}
		stage('build docker image'){
			steps{
				sh 'docker build -t test-1.0 .';
			}

		}
	}
}


