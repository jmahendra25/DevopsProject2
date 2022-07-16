pipeline {
    agent any

    stages {
        stage('GIT Checkout') {
            steps {
                git credentialsId: 'GITHUBcre', url: 'https://github.com/jmahendra25/DevopsProject2.git'
            }
        }
    }
}
