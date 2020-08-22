pipeline {
    agent any
	
    stages {
        stage ('Compile Stage') {

            steps {
             def mvnHome = tool name: 'maven_3_6_3', type: 'maven'
                    sh "${mvnHome}/bin/mvn clean "
            }
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
             
                    sh 'mvn deploy'
            }
        }
    }
}