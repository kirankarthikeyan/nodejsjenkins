pipeline {
    agent any

    tools {
        nodejs "node16"  // Use the name configured in Jenkins > Global Tool Configuration
    }

    stages {
        stage('Checkout Code'){
            steps{
                git branch: 'main', url 'https://github.com/kirankarthikeyan/nodejsjenkins.git '
            }
        }
        stage('Install'){
            steps{
                sh 'npm install'
            }
        }

        stage('Run Tests'){
            steps{
                sh 'npm test'
            }
        }

        
