pipeline {
    agent {
        docker {
            image 'maven:3.9.9-eclipse-temurin-17'
        }
    }

    stages {
        stage('Build') {
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
