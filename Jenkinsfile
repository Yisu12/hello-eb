pipeline {
    agent any

    stages {
        stage('DeployEB') {
            steps {
                withAWS(credentials: 'credenciales-aws', region: 'eu-west-1') {
                    dir('eb'){
                        sh 'eb deploy'
                    }
                }
            }
        }
    }
}
