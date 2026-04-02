pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Docker') {
            steps {
                bat 'docker build -t springboot-app .'
            }
        }
       stage('Deploy') {
    steps {
        bat 'kubectl apply -f deployment.yaml --validate=false'
    }
}
    }
}