pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code from SCM...'
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install' // Installs npm dependencies
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'npm run build' // Run the build script defined in package.json
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh 'npm test' // Run the test script defined in package.json
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'npm run deploy' // Run the deploy script defined in package.json
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
