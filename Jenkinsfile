pipeline {

    agent any

    stages {

        stage("build-docker") {
            
            steps {
                echo 'install dependencies...'
                nodejs('docker') {
                    sh 'docker build -t wwj2547/docker-react-ci -f Dockerfile.dev .'
                }
            }
        }

        stage("test") {
            
            steps {
                echo 'testing the application...'
                nodejs('docker') {
                    sh 'docker run wwj2547/docker-react-ci npm run test -- --coverage'
                }
            }
        }

        stage("deploy") {
            
            steps {
                echo 'deploying the application'
            }
        }
    }

}