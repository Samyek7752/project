
pipeline {
agent {
label {
		label "built-in"
		customWorkspace "/data/project-myapp"
		
		}
		}
		
	stages {
		
		stage ('CLEAN_OLD_M2') {
			
			steps {
				sh "rm -rf root/.m2"
				
			}
			
		}
	
		stage ('MAVEN_BUILD') {
		
			steps {
						
						sh "mvn clean install"
			
			}
			
		
		}
		
		stage ('COPY_WAR_TO_slave_Server'){
		
				steps {
						
						echo "thiss id not done yet, edit here now"

						}
				
				}
	
	
	
	}
		
}
