pipeline {
    agent {
        label {
            label "built-in"
            customWorkspace "/root/data/project-myapp"
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
                // Run Maven build
                sh "mvn clean install /root/data/project-myapp"
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
