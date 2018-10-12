pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // echo 'Building..'
                error("Fail Build")
            }
        }
        stage('Test') {
            steps {
                // echo 'Testing..'
                error("Fail test")
            }
        }
        stage('Deploy') {
            steps {
                // echo 'Deploying....'
                error("Fail deploy")
            }
        }
    }
}
