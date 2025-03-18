pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                g++ -o a p2.cpp
                echo "Build Stage Successful"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                ./a
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
