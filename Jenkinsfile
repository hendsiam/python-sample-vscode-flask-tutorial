pipeline {
    agent any

    environment {
        XYZ = 'ITI ITI ITI'
        IMAGE_NAME = 'hendsiam/jenkins'
    }

    stages {
        stage("Build Docker Image") {
            steps {
                sh "docker build -t ${IMAGE_NAME}:v${BUILD_NUMBER} ."
            }
        }

        stage("Push Docker Image") {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub-cred', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PA
