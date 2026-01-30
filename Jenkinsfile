pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                dir('calculator') {
                    sh './gradlew compileJava'
                }
            }
        }

        stage('Unit Tests') {
            steps {
                dir('calculator') {
                    sh './gradlew test'
                }
            }
        }
    }
}
