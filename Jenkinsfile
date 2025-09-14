pipeline {
    agent {
        docker {
            image 'mcr.microsoft.com/dotnet/sdk:6.0'
        }
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
