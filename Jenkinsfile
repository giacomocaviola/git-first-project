pipeline {
    agent any
    environment {
        TEST_VAR = "test numero 5"
        SERVER_CREDENTIALS = credentials("gitCredentials")
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when {
                expression {
                BRANCH_NAME == 'master'
                }
            }
            steps {
                echo 'Testing..'
                echo "waiting for ${TEST_VAR}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "${SERVER_CREDENTIALS}"
            }
        }
    }
}
