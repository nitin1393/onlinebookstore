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

           mail bcc: 'DevOps test', body: 'Practical', cc: '', from: '', replyTo: '', subject: 'test', to: 'khannanitin106@gmail.com'
        }
    }

}
}
