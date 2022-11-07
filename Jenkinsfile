node{
	stage('SCM Checkout'){
          git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/myproject'
	}
	stage('Test'){
		env.NODE_ENV = "test"
		print "Environment will be : $env.NODE_ENV"

		sh 'node -v'
		sh 'npm prune'
		sh 'npm install'
		sh 'npm test'
	}
	

}
