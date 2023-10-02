def gv

pipeline {
    agent any
    environment {
        VERSION = "1.3.0"
    }
    stages {
        stage('Init') {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }

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
            }
        }

        stage('Deploy') {
            steps {
                script {
                    gv.DeployApp()
                }
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
