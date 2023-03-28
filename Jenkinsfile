pipeline {
    agent any

    parameters {
        string(name: 'BUILD_NUMBER', defaultValue: '', description: 'react app images')
    }

    stages { 
        stage("Initialization") { 
            steps {
                echo "This is bulidTime: ${params.BUILD_NUMBER}"
                sh "docker stop echo ${docker ps -a -q} && docker rm echo ${docker ps -a -q}"
                sh "docker rmi echo ${docker images -q}"
            }
        }

        stage("Pull-Image") {
            steps {
                sh "docker pull pithawatnuckong/python-server"
                sh "docker pull pithawatnuckong/react-web"
            }
        }

        stage("Run-Images"){
            steps { 
                sh "echo ${docker images}"
                sh "docker images"
            }
        }
    }
}