pipeline {

    agent any

    stages {

        stage("install") {
            
            steps {
                echo 'install dependencies...'
                nodejs('Node-18.12') {
                    sh 'npm install'
                }
            }
        }

        stage("test") {
            
            steps {
                echo 'testing the application...'
            }
        }

        stage("deploy") {
            
            steps {
                echo 'deploying the application'
            }
        }
    }

}