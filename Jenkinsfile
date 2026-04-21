pipeline {
    agent { label 'nodejs-20' }

    environment {
        NODE_ENV = 'production'
        PROJECT   = 'calc'
    }

    parameters {
        choice(name: 'DEPLOY_ENV', choices: ['dev', 'staging', 'production'], description: 'Select target environment')
    }

    stages {
        stage('Deploy') {
            when {
                expression { env.NODE_ENV == 'production' }
            }
            input {
                message 'Ready to deploy?'
                ok 'Yes, deploy now'
            }
            steps {
                echo "Deploying ${env.PROJECT} to ${DEPLOY_ENV}"
            }
        }
    }
}


