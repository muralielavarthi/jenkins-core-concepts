pipeline{
    agent {label 'nodejs-20'}

    environment {
        NODE_ENV = 'production'
        PROJECT = 'calc'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    parameters {
        // string - free text input
        string(name: 'APP_VERSION', defaultValue: '1.0.0', description: 'Version of the application to build')

        // choice - dropdown selection
        choice(name: 'DEPLOY_ENV', choices: ['dev', 'staging', 'production'], description: 'Target deployment environment')

        // booleanParam - true/false toggle
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Whether to run tests before deploying')

        // password - masked sensitive input
        password(name: 'DB_PASSWORD', defaultValue: '', description: 'Database password (masked)')

        // text - multi-line input
        text(name: 'RELEASE_NOTES', defaultValue: '', description: 'Release notes for this deployment')
    }
    stages{
        stage('Build') {
            steps {
                echo "Building application version: ${params.APP_VERSION}"
                echo "Using NODE_ENV: ${env.NODE_ENV}"
                echo "Project: ${env.PROJECT}"
            }
        }
        stage('Test') {
            when {
                expression { params.RUN_TESTS == true }
            }
            steps {
                echo "Running tests for version: ${params.APP_VERSION}"
                echo "Project: ${env.PROJECT}"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying ${env.PROJECT} v${params.APP_VERSION} to ${params.DEPLOY_ENV}"
                echo "Release Notes: ${params.RELEASE_NOTES}"
            }
        }
    }
}

