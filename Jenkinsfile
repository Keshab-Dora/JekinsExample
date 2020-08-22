 def mvnHome = tool name: 'maven_3_6_3', type: 'maven'

node {
   
	
   stage('Mvn Package'){
	   // Build using maven
	   
	   sh "${mvnHome} clean package deploy"
   }
   

   stage('Email Notification'){
		mail bcc: '', body: """ You build successfully deployed
		                       Job URL : ${env.JOB_URL}
							   Job Name: ${env.JOB_NAME}
Thanks,
DevOps Team""", cc: '', from: '', replyTo: '', subject: "${env.JOB_NAME} Success", to: 'keshabdora111@gmail.com'
   
   }
}