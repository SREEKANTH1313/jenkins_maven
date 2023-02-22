pipeline {
    agent any
    stages {
        stage('Compile and Clean') {
            steps {
                sh "print mvn clean compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package"
            }
        }
    }
}

