pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/sourabhgorule21/jenkins-demo.git'
            }
        }

        stage('Build Maven') {
            steps {
                sh 'mvn -B clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t demo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop demo-container || true
                docker rm demo-container || true
                docker run -d -p 8081:8080 --name demo-container demo-app
                '''
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed 🚀'
        }
    }
}
