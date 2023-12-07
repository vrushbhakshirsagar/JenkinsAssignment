pipeline {
    agent any  
    stages {
        stage('Checkout') {
            steps {
                script {
                    git 'https://github.com/vrushbhakshirsagar/JenkinsAssignment.git'
                }
            }
        }      
        stage('Build') {
            steps {
                script {
                    bat(script: 'javac HelloWorld.java', returnStatus: true) // Use 'bat' on Windows
                }
            }
        }     
        stage('Test') {
            steps {
                script {
                    bat(script: 'java HelloWorld', returnStatus: true) // Use 'bat' on Windows
                    
                }
            }
        }
    }
    post {
        success {
            echo 'Build successful!'
        }
        
        failure {
            echo 'Build failed!'
        }
    }
}