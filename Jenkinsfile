import groovy.json.JsonSlurper

def config =[:]

pipeline {
    agent any
    stages {
        stage ('Call API'){
            steps{
                withCredentials([usernamePassword(credentialsId: 'GitHubID', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]){
                        config.OUTPUT = script.sh (
                        script: "curl -i -H \"Authorization: token $PASSWORD\" https://api.github.com/users/imran-kkz",
                        returnStdout: true
                    )
                }
            }
        }
        stage ('Parse API Call'){
            steps{
                script{
                def jsonParse = null
                jsonParse = new JsonSlurper().parseText(config.OUTPUT)
                echo jsonParse.name
                }
            }
        }
    }
}
