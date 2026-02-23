pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t yourdockerhubusername/myapp:latest .'
            }
        }
        stage('Push') {
            steps {
                sh 'docker push sudipta351/myapp:latest'
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}