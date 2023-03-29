pipeline {
    agent any

    parameters {
        string(name: 'BUILD_NUMBER', defaultValue: '', description: 'react app images')
    }

    stages { 
        stage("Pull-Image") {
            steps {
                sh "docker pull pithawatnuckong/python-server"
                sh "docker pull pithawatnuckong/react-web"
            }
        }

        stage("Run-Images"){
            steps { 
                sh 'docker images'
                sh 'docker run --name python-server -p 8081:80 -d --rm pithawatnuckong/python-server'
                sh 'docker run --name react-web -p 8082:3000 -d --rm pithawatnuckong/react-web'
                sh 'docker ps'
            }
        }
    }
}