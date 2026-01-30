pipeline {
    agent {
        docker {
            image 'gradle:6.6.1-jre14-openj9'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                dir('calculator') {
                    sh 'gradle compileJava'
                }
            }
        }

        stage('Unit Tests') {
            steps {
                dir('calculator') {
                    sh 'gradle test'
                }
            }
        }
    }
}
