pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/Unkownman06/python-jenkins-ci.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application (e.g., simulate or run script)...'
                sh 'python3 main.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                sh 'python3 -m unittest test_main.py'
            }
        }
    }

    post {
        always {
            echo '📦 Pipeline complete'
        }
        success {
            echo '✅ SUCCESS'
        }
        failure {
            echo '❌ FAILURE'
        }
    }
}
