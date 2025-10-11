pipeline {
    agent any

    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore SeleniumBasicExercise.sln'
            }
        }
        stage('Dotnet build') {
            steps {
                bat 'dotnet build SeleniumBasicExercise.sln --no-restore'
            }
        }
        stage('Run TestProject1') {
            steps {
                bat 'dotnet test TestProject1/TestProject1.csproj --verbosity normal'
            }
        }
    }
}