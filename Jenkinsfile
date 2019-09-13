import groovy.json.JsonSlurper

def out
pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                script {
                        withCredentials([usernamePassword(credentialsId: 'GitHubID', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]){
                            out = sh (
                            script: "curl -H \"Authorization: token $PASSWORD\" https://api.github.com/repos/octocat/Hello-World/pulls/comments",
//                            "curl -H \"Authorization: token $PASSWORD\" https://api.github.com/users/imran-kkz",
                            returnStdout: true
                            )
                        }
                        echo out
                    }
                }
            }
        stage ('Parse API Call'){
            steps{
                script{
                def jsonParse = null
                jsonParse = new JsonSlurper().parseText(out)
                echo jsonParse.user
                echo jsonParse.body
                }
            }
        }
    }
}
