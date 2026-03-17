pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Change Approval') {
            steps {
                sh 'python change_gate.py sample.yaml'
            }
        }
    }
}