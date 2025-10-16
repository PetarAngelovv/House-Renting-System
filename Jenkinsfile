pipeline {
    agent any
    stages {
        stage('Restore project dependencies') {
            steps {
                ba 'dotnet restore' 
            }
        }
        stage('Build the project') { 
            steps {
                bat 'dotnet build --no-restore' 
            }
        }
          stage('Run tests') { 
            steps {
                bat 'dotnet build --no-build --verbosity normal' 
            }
        }
    }
}