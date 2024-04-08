pipeline {
    agent any
    stages {
        stage('Deploy to s3') {
            steps {
                script {
                    echo 'Deploying to S3'
                    sh "aws s3 cp index.html s3://${params.S3BUCKET}/"
                    sh "aws s3 cp css s3://${params.S3BUCKET}/ --recursive"
                    sh "aws s3 cp fonts s3://${params.S3BUCKET}/ --recursive"
                    sh "aws s3 cp img s3://${params.S3BUCKET}/ --recursive"
                    sh "aws s3 cp scss s3://${params.S3BUCKET}/ --recursive"
                    sh "aws s3 cp js s3://${params.S3BUCKET}/ --recursive"
                }
            }
        }
    }
}