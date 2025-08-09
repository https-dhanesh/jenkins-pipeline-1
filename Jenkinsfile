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
                echo "creating build artifact "
                sh 'touch my_file.txt'
            }
        }
        stage('Test') {
            steps{
                echo 'This is the test stage.'
                echo "Testing the presence of the build artifact"
                sh 'ls my_file.txt'
            }
        }
    }
    post{
        always {
            echo 'This will always run, regardless of the build result.'
            cleanWs()
        }
        success {
            echo 'This will run only if the build is successful.'
        }
        failure {
            echo 'This will run only if the build fails.'
        }
    }
}