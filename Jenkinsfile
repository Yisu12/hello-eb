pipeline {
    agent any

    stages {
        stage('DeployEB') {
            steps {
                withAWS(credentials: 'aws-credentials', region: 'eu-west-1') {
                    dir('eb'){
                        sh 'eb deploy'
                    }
                }
            }
        }
    }
}
