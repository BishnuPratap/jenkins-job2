pipeline {
  tools {
    jdk "JAVA_HOME_MASTER"
	maven "M2_HOME_MASTER"
 
  }
    agent any

    stages {
        stage('git clone') {
            steps {
			    git 'https://github.com/ashisnishanka/jenkins-job1.git'
                echo 'git clone completed'
            }
        }
		
	    stage('compile') {
            steps {
			    sh 'mvn compile'
                echo 'compile completed'
            }
        }
		
	    stage('test') {
            steps {
			    sh 'mvn test'
                echo 'test completed'
            }
        }
		
		stage('package') {
            steps {
			    sh 'mvn package'
                echo 'package completed'
            }
        }
		
    }
}
