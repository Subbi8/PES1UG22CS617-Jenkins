pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22SC617-1 main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS617-1'  
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh '''
                    git config --global user.name "Subbi8"
                    git config --global user.email "your-email@example.com"
                    git add main.cpp
                    git commit -m "Added working .cpp file"
                    git push origin main
                    '''
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
