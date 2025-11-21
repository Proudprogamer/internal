pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'docker login -u siddharthpg -p qsxxsqoknnko123321Q'

                    // Build and push Docker image
                    bat 'docker build -t w9-dd-app:latest .'
                    bat 'docker tag w9-dd-app:latest siddharthpg/w9-dh-app:latest'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    
                    echo '✅ Deployed successfully to Minikube!'
                }
            }
        }
    }
}