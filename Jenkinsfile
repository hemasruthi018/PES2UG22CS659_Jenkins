pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec main/hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './Invalid_file'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
