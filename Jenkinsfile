pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'echo "Building the project..."'
                    sh './gradlew build' // Use 'mvn package' for Maven projects
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'echo "Running tests..."'
                    sh './gradlew test' // Replace with 'mvn test' for Maven
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'echo "Deploying the application..."'
                    // Add deployment scripts or commands here
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
