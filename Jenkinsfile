// Declarative pipeline
pipeline {
    agent any

    parameters {
            booleanParam(name: 'build_image', defaultValue: true, description: 'chech to build the docker image')
        }

    stages {

        stage ('Git Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/chetannaik-44/dev_repo.git'
            }
        }
        
        stage ('Build Docker Image') {
            when {
                expression { return params.build_image }
            }
            steps {
                sh 'docker-compose build '       
            }
        }
    }
}