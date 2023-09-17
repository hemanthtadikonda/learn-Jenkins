pipeline {
    agent { node { label 'slave'} }
    environment {
        TEST_URL = "google.com"
        SSH = credentials('centos-ssh')
    }
    options {
        ansiColor('xterm')
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