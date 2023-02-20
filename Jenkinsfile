pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS351 PES1UG20CS351.cpp'
                build job: 'PES1UG20CS351-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS351'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
