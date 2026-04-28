pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sourabhgorule21/jenkins-demo.git'
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
