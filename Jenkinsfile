pipeline{

    agent any
    stages{
    stage('SCM Checkout')
    {
        steps{
        git 'https://github.com/ashishdubey195/phpmysql-app.git'
    }
    }
    
    stage('Run Docker Compose File')
    {
        steps{
        sh 'docker compose build'
        sh 'docker compose up -d'
    }
    }
}
}
