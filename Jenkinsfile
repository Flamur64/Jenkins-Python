pipeline {
    agent {
        label 'docker-agent-python'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/yourrepository.git'
            }
        }
        stage('Build') {
            steps {
                sh 'pip install -r myapp/requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 myapp/tests.py'
            }
        }
        stage('Run') {
            steps {
                sh 'python3 myapp/main.py arg1 arg2'
            }
        }
    }
}
