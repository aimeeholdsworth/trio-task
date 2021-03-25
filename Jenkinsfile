pipeline{
    agent any
    envrionmet{
        MYSQL_ROOT_PASSWORD = credentials("MYSQL_ROOT_PASSWORD")

    }
    stages{
        stage("Build"){
            steps {
                sh "docker-compose build --parrallel"

            }
            
        }
        stage("Push"){
            steps{
            sh "docker-compose push"
            }
        }
        stage("Deploy"){
            steps{
            sh "docker-compose up -d"
            }
        }
    }
}