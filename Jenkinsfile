pipeline{
    agent any

    triggers{
        pollSCM('H/5 * * * *')
    }

    stages{
        stage("Build"){
            steps{
                bat 'dotnet build'
            }
        }
        stage("Test"){
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }

}