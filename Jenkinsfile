pipeline{
    agent any
    
    environment{
        XYZ='ITI ITI ITI'
    }
    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t hendsiam/jenkins:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push hendsiam/jenkins:v${BUILD_NUMBER}"
            }
        }
    }
}
