pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'aws elasticbeanstalk --help | grep create'
            }


        stage('Test') {
            steps {
                sh 'echo "Testing stage"'
            }


        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage"'
            }

        }
    }
}
