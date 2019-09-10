pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                script{
                    sh "curl -i -H \"Authorization: token bd8015227867c497121b985b9477ba3624d13c65\" https://github.com/api/v3/users/imran-kkz" 
                }
            }
        }
    }
}