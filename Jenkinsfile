pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                script{
                    sh "curl -i -H \"Authorization: token 9550fd0cfae8425872af3a8033a26c9864fe4ecc\" https://api.github.com/users/defunkt" 
                }
            }
        }
    }
}
