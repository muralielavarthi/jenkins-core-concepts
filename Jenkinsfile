pipeline {
    agent any

    stages{
        stage("Build"){
            steps{
                """
                sh echo "hello world from build stage"
                """
        }
        stage("Test"){
            steps{
                """
                sh echo "hello world from test stage"
                """
            }
        }
        stage("Deploy"){
            steps{
                """
                sh echo "hello world from deploy stage"
                """
            }
        }
    }
}
}