pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the Git repository
                git url: 'https://github.com/srirath7/hello-world.git'
            }
        }

        stage('Build') {
            steps {
                // Build the application (for example, a Java project)
                sh 'echo "Building the application..."'
                // Replace this with your actual build command, e.g., 'mvn clean install' for a Maven project
            }
        }

        stage('Test') {
            steps {
                // Run tests (for example, unit tests)
                sh 'echo "Running tests..."'
                // Replace this with your actual test command, e.g., 'mvn test' for a Maven project
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (for example, copy files to a server or trigger a deployment script)
                sh 'echo "Deploying the application..."'
                // Replace this with your actual deployment command, e.g., 'scp target/app.jar user@server:/path/to/deploy/'
            }
        }
    }

    post {
        always {
            // Actions to perform regardless of the pipeline result (e.g., cleanup)
            echo 'Cleaning up...'
        }
        success {
            // Actions to perform if the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
