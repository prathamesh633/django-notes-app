pipeline {
    agent {label "slave"}

    stages {
        stage('code') {
            steps {
                sh "sudo yum install git -y"
                git url: "https://github.com/prathamesh633/django-notes-app.git", branch: "main"
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
                sh "sudo docker-compose down && docker-compose up -d"
                echo " Deployment - DONE"
            }
        }
        stage("clean-up"){
            steps{
                sh "sudo docker system prune -a -f"
                echo " Cleaning - DONE"
            }
        }
    }
}
