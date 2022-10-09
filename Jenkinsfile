pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'aws elasticbeanstalk --help | grep create'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Test stage"'
            }
        }


        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage"'
            }
        }

    }
}
