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
        stage('Run TestProject2') {
            steps {
                bat 'dotnet test TestProject2/TestProject2.csproj --verbosity normal'
            }
        }
        stage('Run TestProject3') {
            steps {
                bat 'dotnet test TestProject3/TestProject3.csproj --verbosity normal'
            }
        }
    }
}