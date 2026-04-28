pipeline {
    agent {
        docker {
            image 'maven:3.9.9-eclipse-temurin-21'
            args '-v maven-repo:/root/.m2'
        }
    }

    stages {
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
