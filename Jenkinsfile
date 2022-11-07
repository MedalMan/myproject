node{
	stage('SCM Checkout'){
          git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/myproject'
	}
	stage('build'){
		agent{
			docker{
				image 'node:14-buster'
			}
		}
	}
	steps{
		sh 'yarn install --frozen-lockfile'
		sh 'yarn run build'
		sh 'tar -cvf buildSources.tar ./dist/'
		stash(name: 'dist-files', includes; 'buildSources.tar', userDefaultExcludes: 'true')
	}


}
