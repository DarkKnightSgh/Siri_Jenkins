pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o PES1UG21CS599-1 hello.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Execute the compiled .cpp file and print output
                    sh './PES1UG21CS599-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy stage'
                // Add deployment steps if necessary
            }
        }
    }

    post {
        always {
            // Display 'pipeline failed' in case of any errors within the pipeline
            catchError {
                script {
                    // Add any additional error handling or notifications here
                    echo 'Pipeline succeeded!'
                }
            }
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
