@Library("shared") _
pipeline {
    agent {label "slave"}

    stages {
        stage('code') {
            steps {
                script{
                    code-clone(https://github.com/prathamesh633/django-notes-app.git, main)
                }
                echo "code clone - DONE"
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
                    docker-compose()
                }
                echo " Deployment - DONE"
            }
        }
        stage("clean-up"){
            steps{
                script{
                    cleanup()
                }
                echo " Cleaning - DONE"
            }
        }
    }
}
