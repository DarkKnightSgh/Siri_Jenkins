pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/DarkKnightSgh/Siri_Gowri_H_Jenkins.git'  
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS599-1’,
                sh 'g++ hello2.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
