pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the C++ project...'
                    sh 'g++ -o hello_exec hello.cpp'  // Compiling C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the compiled program...'
                    sh './hello_exec'  // Executing compiled C++ file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment Step: Success!'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed ❌'
        }
    }
}
