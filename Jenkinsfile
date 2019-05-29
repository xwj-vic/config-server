node{
    stage('Checkout') {
        checkout scm
    }

    stage('Test') {
        sh 'ls -la'
    }

    withEnv([
        'SERVICE=config-server',
        'PROFILES=dev'
    ]){
        stage('Build') {
            sh './build.sh'
        }

        stage('Deploy') {
            sh './deploy.sh'
        }
    }


}
