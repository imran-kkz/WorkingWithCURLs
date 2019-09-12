pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                withCredentials([usernamePassword(credentialsId: 'GitHubID', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]){
                    script{
                        sh "curl -i -H \"Authorization: token $PASSWORD\" https://api.github.com/users/imran-kkz" 
                    }
                }
            }
        }
    }
}
