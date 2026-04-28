pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/sourabhgorule21/jenkins-demo.git'
            }
        }

        stage('Verify') {
            steps {
                sh 'echo "Jenkins is working"'
                sh 'ls -la'
            }
        }
    }
}
