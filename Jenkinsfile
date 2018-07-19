pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'cd modules/helloWorld'
                sh 'mvn clean install'
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
                sh 'mvn deploy'
            }
        }
    }
}