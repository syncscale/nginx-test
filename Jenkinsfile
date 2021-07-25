pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cp -a Dockerfile-alpine.template Dockerfile'
                sh 'docker build . --tag nginx:alpine1'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run -itd -p 80:80 -n test nginx:alpine1'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello World'
            }
        }

    }
}
