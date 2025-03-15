pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/DHANUVARSHA04/PES2UG22CS177_jenkins.git'
            }
        }
        stage('Build C++') {
            steps {
                sh 'g++ main/hello.cpp -o output'
                echo 'Build completed successfully'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!!'
        }
    }
}
