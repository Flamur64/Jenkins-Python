pipeline {
    agent {
        node {
            label 'docker-agent-python'
            }
        }
        stage('Checkout') {
            steps {
                git 'https://github.com/Flamur64/Jenkins-Python.git'
            }
        }
        stage('Install Dependencies') {
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
                sh 'python3 myapp/main.py'
            }
        }
    }
}
