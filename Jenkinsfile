pipeline {
    agent any

    stages {
        stage('1. Build Jar Package') {
            steps {
                echo 'Maven is compiling and packaging the second pipeline...'
                bat 'mvn clean package'
            }
        }
        stage('2. Deploy Package (Ansible)') {
            steps {
                echo 'Packaging complete! Deploying artifact package...'
                bat 'mkdir C:\\second-pipeline-deployment || exit 0'
                bat 'copy target\\second-pipeline-1.0.0.jar C:\\second-pipeline-deployment\\app.jar'
                echo 'DEPLOYMENT COMPLETE!'
            }
        }
    }
}