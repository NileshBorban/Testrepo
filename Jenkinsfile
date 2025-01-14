pipeline {
    agent any
    
    stages {
        stage('Initialization') {
            steps {
                echo 'Starting the pipeline...'
            }
        }
        
        stage('Print Environment Variables') {
            steps {
                echo "Jenkins Build Number: ${env.BUILD_NUMBER}"
                echo "Jenkins Job Name: ${env.JOB_NAME}"
                echo "Workspace Path: ${env.WORKSPACE}"
            }
        }
        
        stage('Run a Shell Command') {
            steps {
                echo 'Running a simple shell command:'
                sh 'echo Hello, Jenkins Pipeline!'
            }
        }
        
        stage('Simulate Build') {
            steps {
                echo 'Simulating build process...'
                sh '''
                echo "Building application..."
                sleep 2
                echo "Build completed!"
                '''
            }
        }
        
        stage('Simulate Test') {
            steps {
                echo 'Simulating test process...'
                sh '''
                echo "Running tests..."
                sleep 2
                echo "Tests passed!"
                '''
            }
        }
        
        stage('Simulate Deploy') {
            steps {
                echo 'Simulating deployment process...'
                sh '''
                echo "Deploying application..."
                sleep 2
                echo "Deployment successful!"
                '''
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}
