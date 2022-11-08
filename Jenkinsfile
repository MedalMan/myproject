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
				sh 'docker build -t rahi776/node-app:latest .';
			}
		}
		stage('Push Docker Image'){
			steps{
			    sh 'docker push rahi776/node-app:latest';
			}

		}
	}
}



