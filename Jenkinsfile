
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
"""                when {
                    expression {
                        BRANCH_NAME == 'main'
                    }
                }"""
                echo 'Building the application...'
            }
        }
        stage('Test') {
            steps {
                echo 'IOIOIOIOIOIOIOIOIO'
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
