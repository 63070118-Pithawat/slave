pipeline {
    agent any

    parameters {
        string(name: 'BUILD_NUMBER', defaultValue: '', description: 'react app images')
    }

    stages { 
        stage("Initialization") { 
            steps {
                echo "This is bulidTime: ${params.BUILD_NUMBER}"
            }
        }

        stage("Pull-Image") {
            steps {
                sh "docker pull -t pithawatnuckong/python-server:latest pithawatnuckong/python-server"
                sh "docker pull -t pithawatnuckong/react-web:latest pithawatnuckong/react-web"
            }
        }

        stage("Run-Images"){
            steps { 
                sh "docker images"
            }
        }
    }
}