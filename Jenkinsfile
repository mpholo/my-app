pipeline {
    agent any 
    stages {
        stage('Remove Repo,Clone Repo and clean') {
            steps {
                  sh "mvn clean"
            }
        }
         stage('Tests') {
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
