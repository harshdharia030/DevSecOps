pipeline{
    agent any

    stages{
        stage('Clone Repo'){
           steps{
                git 'https://github.com/harshdhari030/DevSecOps.git'
           }
        }
        stage('Build Docker Image'){
           steps{
                sh 'docker build -t mywebapp .'
           }
        }
        stage('Run Docker Container'){
           steps{
                sh 'docker run -d -p 8080:80 --name we-container mywebapp || true'
           }
        }
    }
}

