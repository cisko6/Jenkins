
pipeline {
    agent any
    environment {
        VERSION = "1.3.0"
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
                withCredentials([
                    usernamePassword(credentialsId: '6f0640b7-66ee-4d3c-9527-b9c452cc8b62', usernameVariable: 'USER', passwordVariable: 'PWD')
                ]) 
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
