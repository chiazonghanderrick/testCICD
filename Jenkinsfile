pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pulls the code from GitHub
                checkout scm
            }
        }

        stage('Lint & Test') {
            steps {
                echo 'Running basic syntax checks...'
                // Example: if using npm, you might run 'npm run lint'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Web Server...'
                // Example: Copying files to an Apache/Nginx folder
                // sh 'cp -R * /var/www/html/'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs.'
        }
    }
}
