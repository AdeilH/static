pipelins{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'echo "Hello World"'
                sh '''
                    echo "Multilineshell steps work too"
                    ls -lah
                '''
            }
        }
    }
}