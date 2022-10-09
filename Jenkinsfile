pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'eb --help'
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
