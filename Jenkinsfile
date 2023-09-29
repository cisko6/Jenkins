
pipeline {
    agent any
    environment {
        VERSION = "1.3.0"
        SERVER_CREDENTIALS = credentials('git:996e1f714b08e971ec79e3bea686287e66441f043177999a13dbc546d8fe402a')
    }
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME == 'main'
                }
            }
            steps {
                echo 'Building the application...'
            }
        }
        stage('Test') {
            steps {
                echo "Testing application with version ${VERSION}"
                echo "My credentials: ${SERVER_CREDENTIALS}"
                sh "${SERVER_CREDENTIALS}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'xd'
            }
        }
    }
    post {
        always {
            echo 'POST - always sa vykonal'
        }
        success {
            script {
                echo 'POST - success sa vykonal'
            }
        }
        failure {
            script {
                echo 'POST - failure sa vykonal'
            }
        }
    }
}
