pipeline {
    agent { label 'nodejs-20' }

    environment {
        DEPLOY_ENV = 'production'
    }

    stages {
        stage('Deploy') {
            when {
                expression { env.DEPLOY_ENV == 'production' }
            }
            input {
                message 'Ready to deploy?'
                ok 'Yes, deploy now'
            }
            steps {
                echo "Deploying ${env.DEPLOY_ENV} environment"
            }
        }
    }
}


