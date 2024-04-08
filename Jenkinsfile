pipeline {
    agent any
    stages {
        stage ('Git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Chriscloudaz/resume-site.git'
            }
        }

        stage('Deploy to s3') {
            steps {
                script {
                    withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'sam-jenkins-demo-credentials', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
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
}