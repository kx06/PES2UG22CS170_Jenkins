pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build "PES2UG22CS170-1"
                    sh 'ls'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'ls -a'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'deploy'
                }
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
