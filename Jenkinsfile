pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                echo 'Cloning repository...'
                git 'https://github.com/SurajSingh0807/mavenproject.git'
            }
        }
        stage('Build'){
            steps{
                echo 'Building...'
                bat 'mvn clean compile'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing...'
                bat 'mvn test'
            }
        }
        stage('Package'){
            steps{
                echo 'Packaging...'
                bat 'mvn package'
            }
        }
    }
    post {
        success {
            echo 'Build completed successfully!'
        }

        failure {
            echo 'Build failed!'
        }
    }
}