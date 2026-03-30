pipeline {
    agent {label 'nodejs-20'}
    environment { #global environment variables
        NODE_ENV = 'production'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                    echo "Build"
                    echo "NODE_ENV: ${env.NODE_ENV}"
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