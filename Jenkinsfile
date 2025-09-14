pipeline {
    agent any   // Локал agent ашиглана
    agent any
    environment {
        PATH = "/usr/local/bin:${env.PATH}"
    }
    stages {
        stage('Restore') {
            steps {
                sh 'dotnet restore Homies.sln'
            }
        }
        stage('Build') {
            steps {
                sh 'dotnet build Homies.sln --no-restore'
            }
        }
        stage('Test') {
            steps {
                sh 'dotnet test Homies.sln --no-build'
            }
        }
    }
}