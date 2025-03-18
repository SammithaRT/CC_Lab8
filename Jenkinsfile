pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                g++ -o PES1UG22SCS514-1 p2.cpp
                echo "Build Stage Successful"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                ./PES1UG22CS514-1
                echo "Test Stage Successful"
                '''
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
