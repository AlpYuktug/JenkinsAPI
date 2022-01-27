pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Restore packages'){
           steps{
               sh 'dotnet restore JenkinsAPI.sln'
            }
         }
        stage('Clean'){
           steps{
               sh 'dotnet clean JenkinsAPI.sln --configuration Release'
            }
         }
        stage('Build'){
           steps{
               sh 'dotnet build JenkinsAPI.sln --configuration Release --no-restore'
            }
         }
        stage('Publish'){
             steps{
               sh 'dotnet publish JenkinsAPI/JenkinsAPI.csproj --configuration Release --no-restore'
             }
        }
    }
}
