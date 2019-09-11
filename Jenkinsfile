pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                script{
                    sh "curl -i -H \"Authorization: token ca37d10fab3467c08ecc773b6eac4a46566d0dbf\" https://api.github.com/users/defunkt" 
                }
            }
        }
    }
}
