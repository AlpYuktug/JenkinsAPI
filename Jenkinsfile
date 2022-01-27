pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Restore packages'){
           steps{
               bat 'dotnet restore JenkinsAPI.sln'
            }
         }
        stage('Clean'){
           steps{
               bat 'dotnet clean JenkinsAPI.sln --configuration Release'
            }
         }
        stage('Build'){
           steps{
               bat 'dotnet build JenkinsAPI.sln --configuration Release --no-restore'
            }
         }
    }
}
