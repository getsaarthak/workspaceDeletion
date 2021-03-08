		pipeline {
		agent any
	 
		stages {
			stage('Build') {
				steps {
					sh '''
						./mvn.sh mvn -B -DskipTests clean package
					'''
				}
				post {
					success {
					   archiveArtifacts artifacts: './target/*.jar', fingerprint: true
					}
				}
			  }

		     }
	      }
