node {
    stage("Checkout") {
        deleteDir()
        checkout scm
    }

    stage("deploy") {
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'AWS', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) 

        sh '''
            eb init continuous-deployment-demo -p "64bit Amazon Linux 2017.09 v2.6.4 running Java 8" --region "ca-central-1"
        '''

    }
}
