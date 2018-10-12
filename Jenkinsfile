pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                try {
                    throw RuntimeException("Fail Build")
                    // echo 'Building..'

                    currentBuild.result = "SUCCESS"
                    echo "Previous build result: ${currentBuild.previousBuild.result}"
                    if (currentBuild.previousBuild.result != null && currentBuild.previousBuild.result.equals("FAILURE")) {
                        slackSend color: 'good', message: "yana build on branch ${env.BRANCH_NAME} back to normal"
                        notifyStatus("👌")
                    }
                } catch (any) {
                    currentBuild.result = "FAILURE"
                    slackSend color: 'danger', message: "yana build failed on branch ${env.BRANCH_NAME}"
                    notifyStatus("😿")
                    throw any
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                //error("Fail test")
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // error("Fail deploy")
            }
        }
    }
}
