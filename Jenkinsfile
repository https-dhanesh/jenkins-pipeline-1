pipeline{
    agent any

    stages{
        stage('Initialization') {
            steps {
                echo 'Initializing the pipeline...'
            }
        }
        stage('Build') {
            steps{
                echo 'This is the build stage.'
                echo "Running the build on : ${env.BUILD_NUMBER}"
            }
        }
        stage('Test') {
            steps{
                echo 'This is the test stage.'
                echo "Dhanesh is Running tests on : ${env.BUILD_NUMBER}"
            }
        }
    }
}