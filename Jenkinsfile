pipeline {
        agent {label 'tomcat'}
	
	stages {
  	   stage('checkout ') {
    		steps {
      			git branch: 'main', url: 'https://github.com/sudheer76R/java-example.git'
    		       }
  		}

  	   stage('Test') {
    		steps {
      			echo 'This is test task. Assume it completed'
    		      }
  		}

  	   stage('Build') {
    		steps {
      			sh 'mvn clean package'
    		      }
  		}

  	   stage('Deploy') {
    		steps {
      			sh 'sudo cp target/*.war /opt/tomcat/apache-tomcat-9.0.68/webapps/'

    		      }
  		}

}


}
