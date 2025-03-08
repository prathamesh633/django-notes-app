pipeline {
    agent {label "slave"}

    stages {
        stage('code') {
            steps {
                sh "sudo yum install git -y"
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prathamesh633/django-notes-app.git/']])
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
                sh "sudo docker-compose up -d"
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
