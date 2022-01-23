pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mvn"
    }

    stages {
        stage('Build') {
            steps {
             
                // Run Maven on a Unix agent.
                sh "mvn  clean package"
        }
    }
    stage('Test')
    {
        steps{
            echo "Testing start App"
        }
    }
    stage("Email Notification")
    {
        steps{
             echo  "mail sent"
        }
    }

    stage("Deployment"){
        steps{
            echo "Deployment"
        }
    }
    stage("Email notification")
    {
        steps{

           mail bcc: '', body: "'Status of \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\''", cc: '', from: '', replyTo: '', subject: "'Jobs status \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\''", to: 'khannanitin106@gmail.com'
        }
    }

}
}
