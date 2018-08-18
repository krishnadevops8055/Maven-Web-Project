#!groovy

node {
	   
	stage('Checkouting'){

          checkout scm
       }

       stage('BuildArtifact'){

          sh 'mvn install'
       }
	   
      //stage('Sonar') {
                    //add stage sonar
                    //sh 'mvn sonar:sonar'
                //}
   
	
	stage('pipelinesyntax'){
		sshagent(['war']){ 
   sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@18.191.29.247:/opt/apache-tomcat-8.0.53/webapps'
		}}
}
