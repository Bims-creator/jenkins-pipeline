pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Replace with your build command
                sh 'echo "Build step"' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
                // Replace with your test command
                sh 'echo "Test step"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Replace with your deploy command
                sh 'echo "Deploy step"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
            // Email notification for success
            emailext(
                subject: "SUCCESS: ${env.JOB_NAME} - Build #${env.BUILD_NUMBER}",
                body: "Good news! The build succeeded.\n\nCheck it out here: ${env.BUILD_URL}",
                to: "your_email@example.com"
            )
        }
        failure {
            echo 'Pipeline failed!'
            // Email notification for failure
            emailext(
                subject: "FAILURE: ${env.JOB_NAME} - Build #${env.BUILD_NUMBER}",
                body: "Unfortunately, the build failed.\n\nPlease check the details here: ${env.BUILD_URL}",
                to: "your_email@example.com"
            )
        }
    }
}
