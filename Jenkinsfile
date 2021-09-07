pipeline {
    agent any

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
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
             steps {
                echo 'always..'
            }
        }
        failure {
             teps {
               echo 'failure..'
            }
        }
        success {
             steps {
               echo 'success!..'
            }
        }
    }
}
