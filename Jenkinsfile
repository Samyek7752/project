pipeline {
    agent {
        label {
            label "built-in"
            customWorkspace "/root/data/project-myapp"
        }
    }
    
    stages {
        
        stage('1.CLEAN_OLD_M2') {
            steps {
                sh "rm -rf /root/.m2"  // Corrected path
            }
        }
    
        stage('2.MAVEN_BUILD') {
            steps {
                // Run Maven build
                sh "mvn clean install"
            }
        }
        
        stage('3.Tomcat_Deploy') {
            steps {
                // Copy WAR file to Tomcat webapps directory
                sh "cp -r /root/data/project-myapp/target/LoginWebApp.war /root/tom/apache-tomcat-9.0.93/webapps"
                
                // Navigate to Tomcat bin directory and start Tomcat
                dir("/root/tom/apache-tomcat-9.0.93/bin") {
                    sh "./startup.sh"
                }
            }
        }
    }
}
