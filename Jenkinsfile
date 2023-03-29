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
                sh "docker images"
            }
        }
    }
}