pipeline {
    agent { label 'Jenkins-agent' }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    stages {
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout Code') {
            steps {
                 git branch:  'main' , credentialsId: 'github', url: 'https://github.com/harikap240/Project1'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         // Add your deployment steps here
        //     }
        // }
    }
}
