pipeline {
    agent any
    environment {
        NEW_VERSION = '1.3.0'
       // SERVER_CREDENTIALS = credentials('github')
    }
    stages {
        stage ("build") {         
            steps {
                echo 'Building the applicaiton'
                echo "Building version ${NEW_VERSION}"
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
                withCredentials ([
                usernamePassword(credentials: 'github', usernameVariable: USER, passwordVariable: PWD )
            ]) {
                sh "some script execution ${USER} and ${PWD}"
            }
            }
        }
    }
}