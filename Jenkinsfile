pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                mvn bundle-support:init
                cd modules/helloWorld
                mvn clean install
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}