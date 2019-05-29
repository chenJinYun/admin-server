node{
    stage('Checkout') {
        checkout scm
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
