pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building"

                   // docker.withRegistry('https://index.docker.io/v1', 'dockerhub-creds-mostafa') {
                     //   def customImage = docker.build("mostafatarek2003/flaskapp:0.0.2")
                       // customImage.push()
                   // }
                }
            }
        }

        stage('Test') {
            agent {
                
                    docker{
                        image 'ubuntu:latest'
             
                }
            }
             steps{echo 'testing'}

        }

        stage('Deploy') {
            input {
                 message 'Do you want to run this container?'
            }
            steps {
                script {
                    echo "Deploying..."
                    sh 'docker run -d --name flaskapp -p 5555:5000 mostafatarek2003/flaskapp:0.0.2'
                }
            }
        }
    }
}

