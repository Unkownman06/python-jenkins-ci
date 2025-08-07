pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/YOUR_USERNAME/python-jenkins-ci.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Python Code') {
            steps {
                sh 'python3 main.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Finished'
        }
        success {
            echo 'SUCCESS ✅'
        }
        failure {
            echo 'FAILED ❌'
        }
    }
}
