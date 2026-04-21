pipeline {
    agent { label 'nodejs-20' }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application'
            }
        }
    }

    post {
        always {
            deleteDir()
        }
    }
}


