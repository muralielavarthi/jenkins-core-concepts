pipeline {
    agent {label 'nodejs-20'}
    environment { 
        NODE_ENV = 'production'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                    echo "Build"
                    echo "NODE_ENV: $NODE_ENV"
                    """
                }
            }
        }
    }
}