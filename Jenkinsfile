pipeline {
    agent any
    environment {
        TEST_URL = "google.com"
    }
    stages {
        stage('compile') {
            steps {
                echo URL
            }
        }
    }
    post {
        always {
            echo 'post'
        }
    }
}