
pipeline {
    agent any

    tools {
        maven 'Maven-3.9'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/venkatnani43/jenkins-springboot-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t springboot-demo:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    docker rm -f springboot-demo || true

                    docker run -d \
                        --name springboot-demo \
                        -p 8080:8080 \
                        springboot-demo:latest
                '''
            }
        }
    }
}
