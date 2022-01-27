pipeline {
    agent any
    triggers {
        githubPush()
    }
        stage('Build'){
           steps{
               sh 'dotnet build JenkinsAPI.sln --configuration Release --no-restore'
            }
         }
    }
}
