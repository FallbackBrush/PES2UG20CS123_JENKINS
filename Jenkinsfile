pipeline {
    agent any
    stages {
        stage('Build')    {
            steps {
                sh 'cd main'
                sh 'g++ hello.cpp -o execute'
                echo 'Build Successful'
            }
        }
        stage('Test')    {
            steps {
                sh './execute'
                echo 'Test Successful'
            }
        }
        stage('Deploy')    {
            steps {
                echo 'Deploy Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
