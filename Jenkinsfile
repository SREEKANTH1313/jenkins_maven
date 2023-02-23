pipeline {
    agent any
    stages {
        stage('Compile and Clean') {
            steps {
                sh "printmvn clean compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
      
        //post { 
        //always { 
           // junit allowEmptyResults:true,testResults:'target/surefire-reports/*.xml'
       // }
   // }
        stage('Deploy') {
            steps {
                sh "mvn package"
            }
        }
        stage('Archving') {
            steps {
                archiveArtifacts '**/target/*.jar'
            }
        }
    }
}

