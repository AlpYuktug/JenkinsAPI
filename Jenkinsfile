pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'dotnet build JenkinsAPI.sln --configuration Release --no-restore'
      }
    }
  }
} 
