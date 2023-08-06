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
    }
}
