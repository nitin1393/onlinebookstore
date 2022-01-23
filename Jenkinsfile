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
            mail  bcc: '', body: 'test \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\'', cc: '', from: '', replyTo: '', subject: 'Hi DevOps \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\'', to: 'khannanitin106@gmail.com'
        }
    }
}
}

post{
    always{
         echo 'I am success now'
    }
}
