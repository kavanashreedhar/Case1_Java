pipeline {
    agent any

    tools {
        maven 'maven'
    }

    environment {
        SCANNER_HOME = tool 'sonar-scanner-latest'

    }

    stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Checkout From Git') {
            steps {
                git branch: 'main', url: 'https://github.com/kavanashreedhar/Case1_Java.git'
            }
        }

        stage('mvn compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('mvn test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
