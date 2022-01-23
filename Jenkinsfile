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
            mail bcc: '', body: 'Hi', cc: '', from: '', replyTo: '', subject: 'Test', to: 'khannanitin106@gmail.com'
        }
    }
}
}
