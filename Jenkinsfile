pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              // bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/Keshab-Dora/JekinsExample.git"
              //  bat "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f JekinsExample"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f JekinsExample"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f JekinsExample"
            }
        }
    }
}
