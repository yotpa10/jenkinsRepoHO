pipeline {
    agent any
    stages {
        stage('clone repo and clean it') {
            steps {
                bat "git clone https://github.com/simplilearn-github/jenkins-repo.git"
                bat "mvn clean -f jenkins-repo"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f jenkins-repo"
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f jenkins-repo"
            }
        }
    }
}
