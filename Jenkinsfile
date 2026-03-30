pipeline {
    agent {label 'nodejs-20'}

    stages {
        stage('Build') {
            steps {
                script {
                    sh """echo "Building..."
                    """
                }
            }
        }
    }
    post {
        always {
            echo 'This will always run after the stage!'
        }
        failure {
            echo 'This will run only if the stage fails.'
        }
        success {
            echo 'This will run only if the stage succeeds.'
        }
    }
}