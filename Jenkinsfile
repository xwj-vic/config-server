node{
    stage('Checkout') {
        git url: 'https://github.com/tw-cloud-native/config-server.git',
            branch: 'master'
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
