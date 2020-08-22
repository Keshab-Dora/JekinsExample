pipeline {
    agent any
	
    stages {
        stage ('Compile Stage') {

            steps {
                    sh "${mvnHome}/bin/mvn clean"
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