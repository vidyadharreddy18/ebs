pipeline {
    agent any
    docker.image('chriscamicas/awscli-awsebcli').inside {
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'AWS', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {

            stage('Prepare environment') {
                sh 'eb init continuous-deployment-demo -p "64bit Amazon Linux 2017.09 v2.6.4 running Java 8" --region "ca-central-1" '
                }
        }
    }
}
