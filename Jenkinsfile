pipeline {
    agent any
    Tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven-3.9.8"
    }
    stages {
        stage('scm') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/saggurthisandeep/TomcatMavenApp.git'
            }
        }
	stage('build') {
            steps {
                   // To run Maven on a Windows agent, use
      		   bat "mvn -Dmaven.test.failure.ignore=true clean package"
	 }	   
      }
   }
}
