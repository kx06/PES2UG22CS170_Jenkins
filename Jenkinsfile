pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build "PES2UG22CS170-1"
                    sh 'g++ ./main/hello.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './output'
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
