pipeline {
    agent any
    tools {
        maven 'Maven' 
        jdk 'JDK25'
    }
    stages {
        stage('Checkout') {
            steps { git 'https://github.com/<username>/<repo>.git' }
        }
        stage('Build') {
            steps { sh 'mvn clean package' }
        }
        stage('Test') {
            steps { sh 'mvn test' }
        }
        stage('Deploy') {
            steps { echo 'Deploying build...' }
        }
    }
}
