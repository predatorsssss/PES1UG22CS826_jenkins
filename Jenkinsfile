pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/predatorsssss/PES1UG22CS826_jenkins.git' 
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG22CS826-1'
                sh 'g++ working.pp -o output'
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
