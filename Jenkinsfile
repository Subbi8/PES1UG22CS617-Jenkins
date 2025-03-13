pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'ls -R'  // Debug: List all files to confirm location
                    sh 'g++ -o PES1UG22SC617-1 CC_TA/hello.cpp'  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22SC617-1'  // Run the compiled binary
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application... (Modify as needed)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
