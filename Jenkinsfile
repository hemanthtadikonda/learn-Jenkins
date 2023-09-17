pipeline {
    agent any
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
                sh 'ansible -i 172.31.42.157, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
            }
        }
    }
    post {
        always {
            echo 'post'
        }
    }
}