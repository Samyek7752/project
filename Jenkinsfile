pipeline {
    agent {
        label {
            label "built-in"
            customWorkspace "/data/project-myapp"
        }
    }
    
    stages {
        
        stage('CLEAN_OLD_M2') {
            steps {
                sh "rm -rf /root/.m2"  // Corrected path
            }
        }
    
        stage('MAVEN_BUILD') {
            steps {
                // Ensure Maven is installed on this node
                sh "mvn clean install"
            }
        }
        
        stage('COPY_WAR_TO_slave_Server') {
            steps {
                // Placeholder for copying WAR to slave server
                echo "This is not done yet, edit here now"
            }
        }
    }
}
