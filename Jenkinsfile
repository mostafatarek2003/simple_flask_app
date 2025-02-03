pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building"

                    
                    docker.withRegistry('https://index.docker.io/v1', 'dockerhub-creds-mostafa') {
                        def customImage = docker.build("mostafatarek2003/flaskapp:0.0.1")
                        customImage.push()
                    }
                }
            }
        }

        stage('Test') {
            steps {
                echo "Testing.."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying.."
            }
        }
    }
}

