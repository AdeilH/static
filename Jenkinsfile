pipeline{
    agent any
    stages{
        stage('Upload to AWS'){
            steps{
                sh 'echo "Hello World"'
                sh '''
                    echo "Multilineshell steps work too"
                    ls -lah
                '''
                withAWS(region:'us-west-2',credentials:'aws-static'){
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'adeel-jenkins-static')
                }
            }
        }
    }
}