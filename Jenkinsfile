pipeline { 
		agent any
		stages { 
			stage ('build') {
				 steps {
						sh 'cp /var/lib/jenkins/workspace/Test/webapp/target/webapp.war /var/lib/tomcat8/webapps'
				 }
				}
				stage ('Test') {
				steps {
						echo 'build'
				 }
				}
				stage ('QA') {
				steps {
						echo 'build'
				 }
				}
				stage ('Deploy') {
				steps {
						echo 'build'
				 }
				}
				stage ('Monitor') {
				steps {
						echo 'build'
				 }
				}
			}
		}
	
