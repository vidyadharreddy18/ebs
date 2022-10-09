pipeline {
   agent any
       stage('Build Code') {
           when {
               branch "master"
           }
           steps {
               sh """
               echo "Building Artifact from Develop Branch"
               """
           }
       }
      stage('Deploy Code') {
           when {
               branch "master"
           }
          steps {
               sh """
               echo "Deploying Code from Develop Branch"
               """
          }
      }
}
