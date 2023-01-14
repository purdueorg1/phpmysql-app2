node{

    stage('SCM Checkout')
    {
        checkout scm
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
    stage('PUSH image to Docker Hub')
    {
        withDockerRegistry([ credentialsId: "dockerHub", url: "" ])
        {
        sh 'docker push vardhanns/phpmysql_app'
        }
    }
}
