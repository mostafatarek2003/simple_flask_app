pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
		script{
			 echo "Building..."
			 def customImage = docker.build("flaskapp:0.0.1")
		}
            }
        }
        
        stage("Test"){
            steps {
                echo "Testing.."
            }
        }
        
        stage("Deploy"){
            steps {
                echo "Deploying.."
            }
        }
    }
}
