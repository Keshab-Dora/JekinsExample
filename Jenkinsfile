 def mvnHome = tool name: 'maven_3_6_3', type: 'maven'

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
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}