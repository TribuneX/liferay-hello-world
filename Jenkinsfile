pipeline {
    agent any

    environment{
        NEXUS_USERNAME = credentials('NEXUS_USERNAME')
        NEXUS_PASSWORD = credentials('NEXUS_PASSWORD')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'cd modules/helloWorld; mvn clean install'
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
                sh 'cd modules/helloWorld; mvn deploy'
            }
        }
    }
}