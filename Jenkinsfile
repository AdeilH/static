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
                withAWS(region:'eu-west-2',credentials:'aws-static'){
                    s3Upload(file:'index.html', bucket:'adeel-jenkins-static', path:'index.html')
                }
            }
        }
    }
}