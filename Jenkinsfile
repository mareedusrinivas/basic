pipeline {
    agent any
    tools {
        jdk 'jdk17' // Replace 'jdk17' with the Name configured in Manage Jenkins > Tools
    }
    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/abhinav761/basic.git',
                    credentialsId: 'github-token'
            }
        }

        stage('Build') {
            steps {
            
                sh 'Sample.java'
            }
        }

        stage('Run') {
            steps {
                sh 'Sample'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the job'
            }
        }
    }
}
