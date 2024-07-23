pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'your-git-credentials-id', url: ''
            }
        }
        stage('Build') {
            steps {
                script {
                    // Restore dependencies
                    sh 'dotnet restore'

                    // Build the application
                    sh 'dotnet build --configuration Release'
                }
            }
    }
}
