pipeline {
    agent any
    environment {
        TEST_VAR = "test numero 5"
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
            }
        }
    }
}
