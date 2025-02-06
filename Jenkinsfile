pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Santha45/Project1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t calculator-app .'
            }
        }

        stage('Test') {
            steps {
                sh 'python -m unittest test_calculator.py'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run --rm calculator-app'
            }
        }
    }
}
