pipeline {
    agent any
    triggers {
        githubPush()
    }
        stage('Build'){
           steps{
               bat 'dotnet build JenkinsAPI.sln --configuration Release --no-restore'
            }
         }
    }
}
