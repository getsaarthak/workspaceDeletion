
		pipeline {
		agent any
		environment {
        	    MyWS = $WORKSPACE
    		}
		stages {
			stage('Build') {
				steps {
					sh '''
						./mvn.sh mvn -B -DskipTests clean package
					'''
				}
				post {
					success {
					   sh '''
					   echo "Deleting Workspace: $current_workspace"
					   echo "BUILD_NUMBER	: $BUILD_NUMBER"
					   echo "BUILD_ID		: $BUILD_ID"
					   echo "BUILD_URL		: $BUILD_URL"
					   echo "NODE_NAME		: $NODE_NAME"
					   echo "JOB_NAME		: $JOB_NAME"
					   echo "BUILD_TAG		: $BUILD_TAG"
					   echo "BUILD_TAG		: $BUILD_TAG"
					   echo "EXECUTOR_NUMBER	: $EXECUTOR_NUMBER"
					   echo "JAVA_HOME		: $JAVA_HOME"
					   echo "WORKSPACE		: $WORKSPACE"	
					   echo "GIT_COMMIT		: $GIT_COMMIT"
					   echo "GIT_URL		: $GIT_URL"
					   echo "GIT_BRANCH		: $GIT_BRANCH"
					   '''
					   //deleteDir()
					}
				}
			  }

		     }
	      }
