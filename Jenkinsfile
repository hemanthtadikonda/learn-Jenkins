pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
            }
        }
    post {
        always {
            echo 'post'
        }
    }
    }
}