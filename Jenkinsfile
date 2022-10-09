pipeline
{
    agent any
    environment
    {
        APP_NAME = 'sample'
        ENVIRONMENT_NAME = 'sample-env'
        REGION = 'us-east-2'
        S3_BUCKET = "artifact"
    }
    stages
    {
        stage('Deploy')
        {
                sh '''
                    eb init --platform node.js --region us-east-2
                '''
            }
}
