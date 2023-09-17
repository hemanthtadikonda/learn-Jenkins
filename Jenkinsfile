pipeline {
    agent any
    environment {
      URL = 'google.com'
    }
    stages {
        stage('compile') {
            steps {
                echo 'URL'
            }
        }
    }
    post {
        always {
            echo 'post'
        }
    }
}