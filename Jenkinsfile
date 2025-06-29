pipeline {
    agent any

    stages {
        stage('Checkout the repository') {
            steps {
                checkout scm
            }
        }
        stage('Restore dependencies') {
            steps {
                 bat 'dotnet restore'
            }
        }
        stage('Build the application') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Test the application') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }

    }
}