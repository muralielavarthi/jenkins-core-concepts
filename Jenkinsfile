pipeline{
    agent {label 'nodejs-20'}
    environment {
        NODE_ENV = 'production'
        PROJECT = 'calc'
    }
    stages{
        stage('Build') {
            steps {
                echo 'Building the application v2'
                echo "Using NODE_ENV: ${env.NODE_ENV}"
                echo "Project: ${env.PROJECT}"
            }
        }
        stage('Test') {
            steps {
                echo "Running tests v2"
                echo "Project: ${env.PROJECT}"
                echo "Using NODE_ENV: ${env.NODE_ENV}"
            }
        }
    }
}

