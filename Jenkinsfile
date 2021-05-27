pipeline {
    agent any
    stages {
        stage ("build") {
            steps {
                echo 'Building the applicaiton'
            }
        }
        stage ("test") {
            steps {
                echo 'Testing the application'
            }
        }
        stage ("Deploy") {
            steps {
                echo 'Deploying the applicaiton'
            }
        }
    }
    post {
        always {
            // The script is always run irrespective of the build status
            echo 'Hey Build is executed'
        }
        success {
            echo 'Hey Build is succesful'
        }
        failure {
            echo 'Hey Build is failed'
        }
    }
}