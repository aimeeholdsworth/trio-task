pipeline{
    agent any
    envrionmet{
        MYSQL_ROOT_PASSWORD = credentials("MYSQL_ROOT_PASSWORD")

    }
    stages{
        stage("Build"){
            sh "docker-compose build --parrallel"
        }
        stage("Push"){
            sh "docker-compose push"
        }
        stage("Deploy"){
            sh "docker-compose up -d"
        }
    }
}