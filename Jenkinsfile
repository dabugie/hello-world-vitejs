pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'developer', url: 'https://github.com/dabugie/hello-world-vitejs.git'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                script {
                    // Build the Docker image using docker-compose
                    sh 'docker-compose build'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker container using docker-compose
                    sh """
                        docker-compose down || true
                        docker-compose up -d
                    """
                }
            }
        }
    }

    post {
        always {
            // Clean up dangling Docker images to free space
            sh 'docker image prune -f'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
