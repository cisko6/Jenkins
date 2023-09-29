CODE_CHANGES = GetGitChanges()
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                when {
                    expression {
                        BRANCH_NAME == 'main' && CODE_CHANGES == true
                    }
                }
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
            echo 'POST - success sa vykonal'
        }
        failure {
            echo 'POST - failure sa vykonal'
        }
    }
}
