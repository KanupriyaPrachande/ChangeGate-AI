pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                sh 'python3 --version || python --version'
            }
        }

        stage('Install Requirements') {
            steps {
                sh 'pip3 install --user -r requirements.txt || pip install --user -r requirements.txt'
            }
        }

        stage('Run') {
            steps {
                sh 'python3 change_gate.py sample.yaml || python change_gate.py sample.yaml'
            }
        }
    }
}