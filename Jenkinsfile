pipeline {
    agent {
        docker {
            image 'maven:3.9.9-eclipse-temurin-17'
            args '-v maven-repo:/root/.m2'
        }
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
