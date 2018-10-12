pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                slackSend color: 'good', message: "Test for Slack Jenkins plugin"
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                //error("Fail test")
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // error("Fail deploy")
            }
        }
    }
}
