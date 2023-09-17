pipeline {
    agent any
    environment {
        TEST_URL = "google.com"
        SSH = credentials('centos-ssh')
    }
    stages {
        stage('compile') {
            steps {
                echo TEST_URL
                echo SSH
                sh 'env'
            }
        }
    }
    post {
        always {
            echo 'post'
        }
    }
}