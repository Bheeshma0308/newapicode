pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: '', url: 'https://github.com/Bheeshma0308/newapicode.git'
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
