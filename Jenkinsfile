pipeline{
    agent {label 'nodejs-20'}
    stages{
        stage('Build') {
            steps {
                echo 'Building the application v2'
            }
        }
        stage('Test') {
            steps {
                echo "Running tests v2"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application v2"
            }
        }
    }
}