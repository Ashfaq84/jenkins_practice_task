pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    environment {
        //variables defined here can be used by any stage
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
                bat 'nvm install'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
    
    post {
        always {
            // this action will happen always regardless of the result of build
            echo 'Post build condition running'
        }
        failure {
            // this action will happen only if the build has failed
            echo 'Post Action if Build Failed'
        }
    }
}
