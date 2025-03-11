pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output PES1UG22AM036.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

