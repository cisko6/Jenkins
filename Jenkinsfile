
pipeline {
    agent any
    environment {
        VERSION = "1.3.0"
        SERVER_CREDENTIALS = credentials('github')
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
