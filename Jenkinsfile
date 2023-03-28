pipeline {
    agent any

    parameters {
        string(name: 'REACT_APP_IMAGE', defaultValue: '', description: 'react app images')
        choice(name: 'PYTHON_APP_IMAGE', defaultValue: '', description: 'python server app')
    }

    stages { 
        stage("Initialization") { 
            steps {
                echo "This is react image: ${REACT_APP_IMAGE}"
                echo "This is python image: ${PYTHON_APP_IMAGE}"
            }
        }

        stage("Pull-Image") {
            steps {
                sh "docker pull ${PYTHON_APP_IMAGE}"
                sh "docker pull ${PYTHON_APP_IMAGE}"
            }
        }

        stage("Run-Images"){
            steps { 
                sh "echo docker images"
            }
        }
    }
}