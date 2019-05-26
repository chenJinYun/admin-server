node{
    stage('Checkout') {
        git url: 'https://github.com/tw-cloud-native/admin-server.git',
            branch: 'master'
    }

    stage('Test') {
        sh 'ls -la'
    }

    withEnv([
        'SERVICE=admin-server',
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
