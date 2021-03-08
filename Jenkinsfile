		pipeline {
		agent any
	 
		stages {
			stage('Build') {
				steps {
					sh '''
						./java-app/mvn.sh mvn -B -DskipTests clean package
					'''
				}
				post {
					success {
					   archiveArtifacts artifacts: 'java-app/target/*.jar', fingerprint: true
					}
				}
			  }

		     }
	      }
