pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'make build' // Replace with your build command
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh 'make test' // Replace with your test command
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'make deploy' // Replace with your deploy command
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
