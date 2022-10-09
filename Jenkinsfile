pipeline {
    agent any
    stages {
        docker.image('amazon/aws-cli').inside {
            withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'AWS', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {

                stage('Prepare environment') {
                    sh 'aws elasticbeanstalk --help'
                }
            }
        }

    }
}
