pipeline {
    agent any 
    stages {
        stage('Remove Repo,Clone Repo and clean') {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/mpholo/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
         stage('Tests') {
            steps {
                sh "mvn test -f my-app"
            }
        }
         stage('Deploy') {
            steps {
               sh "mvn package -f my-app" 
            }
        }
    }
}
