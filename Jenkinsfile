pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'cp -a Dockerfile-alpine.template Dockerfile'
                echo 'docker build . --tag nginx:alpine1'
            }
        }
        stage('Test') {
            steps {
                echo 'docker run -itd -p 80:80 -n test nginx:alpine1'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello World'
            }
        }

    }
}
