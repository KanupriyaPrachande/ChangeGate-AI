pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Fetching code from GitHub..."
            }
        }

        stage('Build') {
            steps {
                echo "Building Change Approval System..."
            }
        }

        stage('Test Approval Rules') {
            steps {
                script {
                    def action = "update"
                    def environment = "production"

                    if (action == "delete" && environment == "production") {
                        error("❌ Deletion in production is not allowed")
                    } else {
                        echo "✅ Approved"
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying..."
            }
        }
    }
}