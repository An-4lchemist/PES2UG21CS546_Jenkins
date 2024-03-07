pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS546-1'
                sh 'g++ code.cpp -o exe_file'
            }
        }
        stage('Test') {
            steps {
                sh './exe_file'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
