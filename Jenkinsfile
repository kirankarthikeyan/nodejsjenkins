pipeline {
    agent any

    tools {
        nodejs "node16"  // Use the name configured in Jenkins > Global Tool Configuration
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/shafnajasir234/nodejsjenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Application') {
            steps {
                echo 'No build step needed for basic Node.js app'
                // For React/Vue apps: npm run build
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy step goes here'
                // Example: sh 'scp -r . user@server:/var/www/app'
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Something went wrong!'
        }
    }
}
