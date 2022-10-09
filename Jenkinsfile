node {
  stage("Checkout") {
    deleteDir()
    checkout scm
  }

  withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'AWS', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
      stage('Prepare environment') {
        sh 'eb init continuous-deployment-demo -p "64bit Amazon Linux 2017.09 v2.6.4 running Java 8" --region "ca-central-1" '
        // Since AWS failed on create if environment already exists, try/catch block allow to continue deploy without failing
        try {
          sh 'eb create jenkins-env --single'
        } catch(e) {
          echo "Error while creating environment, continue..., cause: " + e
        }
        sh 'eb use jenkins-env'
        sh 'eb setenv SERVER_PORT=5000'
      }
      // Ready to deploy our new version !
      stage('Deploy') {
        sh 'eb deploy'
        sh 'eb status'
      }
    }
}
