pipeline {

    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Compile') {
            steps {
                bat 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }

    }

    post {

        success {

            archiveArtifacts artifacts: 'target/*.jar'

        }

    }

}
