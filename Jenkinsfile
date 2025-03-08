@Library("shared") _
pipeline {
    agent {label "slave"}

    stages {
        stage('code') {
            steps {
                script{
                    gitcheckout("https://github.com/prathamesh633/django-notes-app.git", "main")
                }
            }
        }
        stage("build"){
            steps{
                sh """ 
                """
                echo "code clone - DONE"
            }
        }
        stage("test"){
            steps{
                sh ""
                echo "Testing - DONE"
            }
        }
        stage("deploy"){
            steps{
                script{
                    docker_compose()
                }
            }
        }
        stage("clean-up"){
            steps{
                script{
                    cleanup()
                }
            }
        }
    }
}
