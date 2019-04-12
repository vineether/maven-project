pipeline { 
		agent any
		stages { 
			stage ('one') {
				 steps {
						echo 'build one'
				 }
				}
				stage ('two') {
						steps{
						
					 input('do you wna to proceed')
						}
				}
				stage ('three') when{
						not {
							branch "master"
						}
					
				steps{
					echo 'else three'
				}
				}
				stage ('four') {
				pararell { // both the below stages will run parallely
					stage('Unit Test') {
					echo "Running the unit testing"
					}
				}
				
				stage('Integration Test') {
					agent {
						docker {
								reuseNode false // this docker conatiner will run only on this docker agent
								image 'ubuntu'
						}
					}
					steps{
						echo 'running integration testing'
						}
				
				
					}
				}
