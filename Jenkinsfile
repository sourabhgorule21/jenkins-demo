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

        stage('Build Maven') {
            steps {
                sh 'mvn -B clean package'
            }
        }
    }

    post {
        always {
            echo 'Build completed'
        }
    }
}
