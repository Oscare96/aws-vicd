pipeline {
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/Oscare96/aws-vicd.git'
        IMAGE_TAG = 'oscar996/cicd'
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: "${BRANCH_NAME}", url: '${GIT_URL}'
            }
        }
        stage('docker build') {
            steps {
                 sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
                sh 'docker image'
            }
        }
    }
}